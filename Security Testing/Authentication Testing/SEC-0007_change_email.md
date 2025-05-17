## **SEC-0006:** Authentication Testing - Change Email

> **Summary:** Verify that the Verch web application's email change process functions correctly, ensuring users can successfully update their email addresses while maintaining proper security and providing a good user experience.

**Preconditions:**

- Tester has access to the Verch web application
- Tester has active user accounts with verified email addresses
- Tester has access to both original and new email addresses for testing
- Email verification system is properly configured
- Test environment is capable of sending emails or has a mock email service

### 1. Email Change UI and Access

| #   | Test Description                 | Test Steps                                                     | Expected Behavior                                             |
| --- | -------------------------------- | -------------------------------------------------------------- | ------------------------------------------------------------- |
| 1.1 | Email Change Option Availability | Navigate to user account or profile settings                   | Email change option is clearly accessible in account settings |
| 1.2 | UI Components                    | Examine email change form elements                             | Form includes current email display and new email input       |
| 1.3 | Access Protection                | Attempt to access email change functionality                   | Appropriate authentication is required before changing email  |
| 1.4 | Form Validation                  | Submit email change form with various inputs                   | Form validation provides clear feedback on invalid entries    |
| 1.5 | Accessibility                    | Test email change using keyboard navigation and screen readers | Process is fully accessible with proper labels and navigation |

### 2. Security Verification for Email Change

| #   | Test Description           | Test Steps                                       | Expected Behavior                                              |
| --- | -------------------------- | ------------------------------------------------ | -------------------------------------------------------------- |
| 2.1 | Password Verification      | Check if password is required for email change   | System requires password verification before email change      |
| 2.2 | Current Email Verification | Check if verification is sent to current email   | System sends confirmation to current email before changing     |
| 2.3 | Two-Factor Authentication  | Test email change with 2FA enabled account       | 2FA is required during email change if enabled for account     |
| 2.4 | Session Validation         | Attempt email change from new/suspicious session | Additional verification for suspicious sessions if implemented |
| 2.5 | Rate Limiting              | Attempt multiple email changes in succession     | System implements rate limiting on email change requests       |

### 3. Verification Process Flow

| #   | Test Description           | Test Steps                                           | Expected Behavior                                          |
| --- | -------------------------- | ---------------------------------------------------- | ---------------------------------------------------------- |
| 3.1 | Current Email Notification | Initiate email change process                        | Notification sent to current email about requested change  |
| 3.2 | New Email Verification     | Complete initial steps of email change               | Verification link sent to new email address                |
| 3.3 | Verification Link Security | Analyze verification links in emails                 | Links contain secure, properly signed, and expiring tokens |
| 3.4 | Complete Change Process    | Follow verification links in both emails if required | Email change completes only after all verifications        |
| 3.5 | Cancelation Option         | Check if email change can be canceled during process | Option to cancel email change before completion            |

### 4. Email Change Implementation

| #   | Test Description             | Test Steps                                               | Expected Behavior                                             |
| --- | ---------------------------- | -------------------------------------------------------- | ------------------------------------------------------------- |
| 4.1 | Database Update              | Complete email change and check database (if accessible) | Email is updated in database only after complete verification |
| 4.2 | Login with New Email         | Attempt login with new email after change                | Login works with new email address after change               |
| 4.3 | Login with Old Email         | Attempt login with old email after change                | Old email no longer works for authentication                  |
| 4.4 | Verification Status Transfer | Check verification status of new email                   | New email inherits or requires verification based on policy   |
| 4.5 | Associated Records Update    | Check if email is updated in all associated records      | Email change propagates to all relevant system records        |

### 5. User Experience and Feedback

| #   | Test Description            | Test Steps                                        | Expected Behavior                                            |
| --- | --------------------------- | ------------------------------------------------- | ------------------------------------------------------------ |
| 5.1 | Email Change Notifications  | Complete email change process                     | Users receive clear notifications at each step               |
| 5.2 | Success Confirmation        | Complete full email change process                | Clear success message confirms email change completion       |
| 5.3 | Process Progress Indication | Observe UI during multi-step email change process | Progress indicators show current stage in multi-step process |
| 5.4 | Error Message Clarity       | Trigger various errors during email change        | Error messages are clear, specific, and actionable           |
| 5.5 | Mobile Responsiveness       | Complete email change on mobile device            | Process works correctly on mobile devices                    |

### 6. Security Implications

| #   | Test Description          | Test Steps                                             | Expected Behavior                                                |
| --- | ------------------------- | ------------------------------------------------------ | ---------------------------------------------------------------- |
| 6.1 | Active Sessions Handling  | Change email and check existing sessions               | System either maintains or invalidates sessions based on policy  |
| 6.2 | Security Notification     | Complete email change                                  | Security notifications sent to both old and new emails           |
| 6.3 | Account Recovery Options  | Check account recovery options after email change      | Account recovery options update to reflect new email             |
| 6.4 | Connected Services Update | Check if email change affects connected services/OAuth | Connected services handle email change appropriately             |
| 6.5 | Fraud Prevention Measures | Change to suspicious email pattern                     | System implements additional verification for suspicious changes |

### 7. Edge Cases and Error Handling

| #   | Test Description                   | Test Steps                                           | Expected Behavior                                             |
| --- | ---------------------------------- | ---------------------------------------------------- | ------------------------------------------------------------- |
| 7.1 | Change to Already Registered Email | Attempt to change to an email already in system      | System prevents change to already registered email            |
| 7.2 | Expired Verification Links         | Wait for verification links to expire before using   | System handles expired links with clear messaging             |
| 7.3 | Network Interruption               | Interrupt network during email change process        | System handles interruptions gracefully with recovery options |
| 7.4 | Concurrent Email Change Requests   | Initiate second email change before completing first | System handles concurrent change requests appropriately       |
| 7.5 | Cross-Browser Compatibility        | Test email change across different browsers          | Process works consistently across browsers                    |

**Post-conditions:**

- User's email address is successfully changed in the system
- New email is correctly recorded in all relevant database tables
- User can log in with new email address
- Old email address no longer provides authentication
- Appropriate notifications have been sent to both old and new emails
- Email change is securely implemented with proper verification steps
