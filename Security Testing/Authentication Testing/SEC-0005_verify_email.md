## **SEC-0005:** Authentication Testing - Verify Email

> **Summary:** Verify that the Verch web application's email verification process functions correctly, ensuring users can successfully verify their email addresses while maintaining proper security and providing a good user experience.

**Preconditions:**

- Tester has access to the Verch web application
- Tester has newly created user accounts that require email verification
- Tester has access to the email accounts associated with test users
- Email verification system is properly configured
- Test environment is capable of sending emails or has a mock email service

### 1. Email Verification Notification

| #   | Test Description                 | Test Steps                                               | Expected Behavior                                              |
| --- | -------------------------------- | -------------------------------------------------------- | -------------------------------------------------------------- |
| 1.1 | Verification Email Delivery      | 1. Create new account<br>2. Check associated email inbox | Verification email is sent immediately after registration      |
| 1.2 | Email Content and Format         | Examine verification email content                       | Email contains clear instructions and properly formatted link  |
| 1.3 | Email Sender Information         | Check sender details of verification email               | From address and sender name are legitimate and recognizable   |
| 1.4 | Email Subject Line               | Review subject line of verification email                | Subject clearly indicates purpose of email                     |
| 1.5 | Rich Text and Plain Text Support | View email in different email clients                    | Email displays properly in both rich text and plain text modes |

### 2. Verification Link Security

| #   | Test Description          | Test Steps                                           | Expected Behavior                                          |
| --- | ------------------------- | ---------------------------------------------------- | ---------------------------------------------------------- |
| 2.1 | Token Security            | Analyze verification token in email link             | Token is secure, properly signed, and sufficiently complex |
| 2.2 | Token Expiration          | Wait for token expiration period and try to use link | Expired tokens are rejected with clear expiration message  |
| 2.3 | Single-Use Token          | Use verification link twice                          | Link can only be used once, with clear message on reuse    |
| 2.4 | HTTPS Enforcement         | Check if verification link uses HTTPS                | All verification links use HTTPS protocol                  |
| 2.5 | Token Tampering Detection | Attempt to modify verification token                 | System detects and rejects tampered tokens                 |

### 3. Verification Process Flow

| #   | Test Description                   | Test Steps                                               | Expected Behavior                                            |
| --- | ---------------------------------- | -------------------------------------------------------- | ------------------------------------------------------------ |
| 3.1 | Standard Verification Process      | Click verification link in email                         | Account is verified with clear success message               |
| 3.2 | Automatic Login After Verification | Click verification link and observe authentication state | System behavior follows business rules (auto-login or not)   |
| 3.3 | Redirect After Verification        | Complete verification and observe redirect               | User is redirected to appropriate page after verification    |
| 3.4 | Verification Status Persistence    | Verify email and log out and back in                     | Verification status is correctly persisted across sessions   |
| 3.5 | Database Status Update             | Verify email and check database status (if accessible)   | Database correctly records verification status and timestamp |

### 4. User Experience and Feedback

| #   | Test Description            | Test Steps                                        | Expected Behavior                                      |
| --- | --------------------------- | ------------------------------------------------- | ------------------------------------------------------ |
| 4.1 | Success Message Clarity     | Complete verification process                     | Clear success message confirms email verification      |
| 4.2 | Error Message Clarity       | Trigger verification errors (expired, used token) | Error messages are clear, specific, and actionable     |
| 4.3 | Verification UI             | Observe UI elements during verification process   | UI is intuitive with appropriate loading states        |
| 4.4 | Mobile Responsiveness       | Complete verification on mobile device            | Verification process works correctly on mobile devices |
| 4.5 | Cross-Browser Compatibility | Test verification in different browsers           | Verification works consistently across browsers        |

### 5. Resend Verification Email

| #   | Test Description                  | Test Steps                                                  | Expected Behavior                                       |
| --- | --------------------------------- | ----------------------------------------------------------- | ------------------------------------------------------- |
| 5.1 | Resend Functionality Availability | Check for resend option for unverified accounts             | Resend option is clearly available to unverified users  |
| 5.2 | Resend Cooldown/Throttling        | Attempt to resend verification multiple times in succession | System implements appropriate rate limiting             |
| 5.3 | New Token Generation              | Resend verification and examine new token                   | New verification token is generated for resent emails   |
| 5.4 | Old Token Invalidation            | Resend verification and try old token                       | Previously issued tokens are invalidated when resending |
| 5.5 | Resend Confirmation Message       | Request verification email resend                           | Clear confirmation message that email has been resent   |

### 6. System Notifications and Restrictions

| #   | Test Description                    | Test Steps                                                 | Expected Behavior                                          |
| --- | ----------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| 6.1 | Unverified Account Access           | Attempt to access restricted areas with unverified account | Appropriate access restrictions for unverified accounts    |
| 6.2 | Verification Reminder Notifications | Log in with unverified account                             | System displays verification reminders to unverified users |
| 6.3 | Grace Period Implementation         | Check if unverified accounts have usage grace period       | Grace period policy is correctly enforced if implemented   |
| 6.4 | Account Suspension for Unverified   | Leave account unverified beyond maximum allowed time       | Account is handled according to policy after grace period  |
| 6.5 | Verification Status Indicators      | Check for visual indicators of verification status         | Clear visual indicators of account verification status     |

### 7. Edge Cases and Error Handling

| #   | Test Description                  | Test Steps                                                           | Expected Behavior                                              |
| --- | --------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------- |
| 7.1 | Verification with Closed Session  | Close browser session after requesting verification, then click link | Verification succeeds even with new session                    |
| 7.2 | Verification for Deleted Account  | Delete account, then try verification link                           | System handles verification for non-existent accounts          |
| 7.3 | Email Client Link Filtering       | Test verification links through email clients with link protection   | Links work despite email client security measures              |
| 7.4 | Network Interruption              | Interrupt network during verification process                        | System handles interruptions gracefully with recovery options  |
| 7.5 | Verification for Already Verified | Try verification link for already verified account                   | System provides clear message that account is already verified |

**Post-conditions:**

- User's email address is successfully verified in the system
- Verification status is correctly recorded in the database
- User can access all features that require email verification
- Verification tokens are properly invalidated after use
- User receives appropriate confirmation of verification status
