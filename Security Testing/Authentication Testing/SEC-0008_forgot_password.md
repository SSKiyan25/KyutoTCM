## **SEC-0007:** Authentication Testing - Forgot Password

> **Summary:** Verify that the Verch web application's password reset process functions correctly, ensuring users can securely regain access to their accounts when they forget their passwords while maintaining proper security and providing a good user experience.

**Preconditions:**

- Tester has access to the Verch web application
- Tester has active user accounts with verified email addresses
- Tester has access to the email accounts associated with test users
- Password reset system is properly configured
- Test environment is capable of sending emails or has a mock email service

### 1. Password Reset Request UI

| #   | Test Description        | Test Steps                                                   | Expected Behavior                                             |
| --- | ----------------------- | ------------------------------------------------------------ | ------------------------------------------------------------- |
| 1.1 | Reset Link Availability | Examine login page for forgot password option                | Reset password link is clearly visible on login page          |
| 1.2 | Reset Request Form      | Navigate to forgot password page                             | Form provides clear instructions and email input field        |
| 1.3 | Form Validation         | Submit invalid inputs to reset form                          | Form validates input with helpful error messages              |
| 1.4 | User Guidance           | Review instructions on password reset page                   | Clear guidance explains password reset process                |
| 1.5 | Accessibility           | Test reset form using keyboard navigation and screen readers | Process is fully accessible with proper labels and navigation |

### 2. Security Measures for Reset Requests

| #   | Test Description               | Test Steps                                                   | Expected Behavior                                          |
| --- | ------------------------------ | ------------------------------------------------------------ | ---------------------------------------------------------- |
| 2.1 | Rate Limiting                  | Submit multiple reset requests in succession                 | System implements rate limiting on password reset requests |
| 2.2 | CAPTCHA Integration            | Observe if CAPTCHA is required for reset requests            | CAPTCHA is implemented for reset requests if configured    |
| 2.3 | Account Enumeration Prevention | Submit reset requests for existing and non-existing accounts | Generic message displayed regardless of account existence  |
| 2.4 | IP-based Throttling            | Submit many reset requests from same IP                      | System limits excessive requests from same IP address      |
| 2.5 | Account Locking Integration    | Check if reset requests affect account lockout status        | Reset requests don't unlock temporarily locked accounts    |

### 3. Reset Email Delivery

| #   | Test Description        | Test Steps                                     | Expected Behavior                                            |
| --- | ----------------------- | ---------------------------------------------- | ------------------------------------------------------------ |
| 3.1 | Email Delivery          | Submit valid reset request                     | Reset email is delivered promptly to user's email            |
| 3.2 | Email Content           | Examine reset email content                    | Email contains clear instructions and secure reset link      |
| 3.3 | Email Sender Info       | Check sender details of reset email            | From address and sender name are legitimate and recognizable |
| 3.4 | Email Subject           | Review subject line of reset email             | Subject clearly indicates purpose without revealing too much |
| 3.5 | Multiple Email Requests | Request multiple reset emails for same account | System handles multiple requests appropriately               |

### 4. Reset Token Security

| #   | Test Description          | Test Steps                                           | Expected Behavior                                          |
| --- | ------------------------- | ---------------------------------------------------- | ---------------------------------------------------------- |
| 4.1 | Token Complexity          | Analyze reset token in email link                    | Token is secure, properly signed, and sufficiently complex |
| 4.2 | Token Expiration          | Wait for token expiration period and try to use link | Expired tokens are rejected with clear expiration message  |
| 4.3 | Single-Use Token          | Use reset link twice                                 | Link can only be used once, with clear message on reuse    |
| 4.4 | HTTPS Enforcement         | Check if reset link uses HTTPS                       | All reset links use HTTPS protocol                         |
| 4.5 | Token Tampering Detection | Attempt to modify reset token                        | System detects and rejects tampered tokens                 |

### 5. Password Reset Flow

| #   | Test Description         | Test Steps                                            | Expected Behavior                                          |
| --- | ------------------------ | ----------------------------------------------------- | ---------------------------------------------------------- |
| 5.1 | Reset Form UI            | Click valid reset link                                | Secure form is presented for entering new password         |
| 5.2 | Password Requirements    | Attempt to set new password with various strengths    | Form enforces password strength policy with clear guidance |
| 5.3 | Password Confirmation    | Test password and confirmation mismatch               | System validates that passwords match with clear errors    |
| 5.4 | Successful Reset Process | Complete password reset with valid token and password | Password is successfully changed with confirmation message |
| 5.5 | Navigation After Reset   | Complete password reset and observe redirect          | User is redirected to login or automatically logged in     |

### 6. Account Security Implications

| #   | Test Description             | Test Steps                                            | Expected Behavior                                             |
| --- | ---------------------------- | ----------------------------------------------------- | ------------------------------------------------------------- |
| 6.1 | Active Sessions Invalidation | Reset password while having active sessions elsewhere | All existing sessions are invalidated after password reset    |
| 6.2 | Security Notification        | Complete password reset                               | Security notification sent about successful password change   |
| 6.3 | Previous Password Rejection  | Try to set new password identical to old password     | System prevents reuse of previous password if policy requires |
| 6.4 | Password History Enforcement | Try to cycle through passwords to reuse old password  | Password history policy is enforced if implemented            |
| 6.5 | Account Unlock Integration   | Check if password reset affects locked account status | System behavior follows business rules for locked accounts    |

### 7. Edge Cases and Error Handling

| #   | Test Description              | Test Steps                                             | Expected Behavior                                             |
| --- | ----------------------------- | ------------------------------------------------------ | ------------------------------------------------------------- |
| 7.1 | Reset for OAuth-only Accounts | Request password reset for accounts using only OAuth   | System provides appropriate guidance for OAuth-only accounts  |
| 7.2 | Concurrent Reset Requests     | Initiate multiple reset requests before completing any | Latest reset token is valid, older tokens are invalidated     |
| 7.3 | Network Interruption          | Interrupt network during reset process                 | System handles interruptions gracefully with recovery options |
| 7.4 | Cross-Browser Compatibility   | Test reset process across different browsers           | Process works consistently across browsers                    |
| 7.5 | Mobile Responsiveness         | Complete password reset on mobile device               | Process works correctly on mobile devices                     |

**Post-conditions:**

- User can successfully reset their password
- New password is securely stored in the system
- User can authenticate with the new password
- Old password no longer works for authentication
- All active sessions are invalidated (based on security policy)
- Appropriate security notifications are sent to the user
