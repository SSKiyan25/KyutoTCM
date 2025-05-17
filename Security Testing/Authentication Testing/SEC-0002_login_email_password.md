## **SEC-0002:** Authentication Testing - Log in with Email/Password

> **Summary:** Verify that users can successfully log in to the Verch web application using email and password authentication, ensuring proper validation, security measures, and user feedback.

**Preconditions:**

- Tester has access to the Verch web application login page
- Tester has valid registered user credentials (email and password)
- Internet connection is stable
- Test environment is properly configured
- Test accounts of various types and statuses are available (standard, admin, suspended, etc.)

### 1. Basic Login Functionality

| #   | Test Description                | Test Steps                                                                                    | Expected Behavior                                              |
| --- | ------------------------------- | --------------------------------------------------------------------------------------------- | -------------------------------------------------------------- |
| 1.1 | Standard Login Process          | 1. Navigate to login page<br>2. Enter valid email & password<br>3. Submit                     | User is authenticated and redirected to appropriate dashboard  |
| 1.2 | Required Field Validation       | 1. Submit form with empty fields<br>2. Submit with only email<br>3. Submit with only password | Form shows appropriate validation errors for each scenario     |
| 1.3 | Case Sensitivity                | Test email and password with different letter cases                                           | Email is case-insensitive, password is case-sensitive          |
| 1.4 | Form Accessibility              | Test form using keyboard navigation and screen readers                                        | Form is fully accessible with proper labels and tab navigation |
| 1.5 | Login with Different User Types | Test login with different user role accounts                                                  | Each user type is directed to appropriate dashboard/section    |

### 2. Security Measures

| #   | Test Description         | Test Steps                                  | Expected Behavior                                              |
| --- | ------------------------ | ------------------------------------------- | -------------------------------------------------------------- |
| 2.1 | Failed Login Attempts    | Enter incorrect password multiple times     | Account locks after predetermined number of failed attempts    |
| 2.2 | Password Masking         | Check password field during entry           | Password is properly masked with option to toggle visibility   |
| 2.3 | Session Security         | Login and examine session tokens/cookies    | Secure, HTTPOnly flags set on session cookies when appropriate |
| 2.4 | SQL Injection Prevention | Test login form with SQL injection attempts | System sanitizes inputs and prevents SQL injection attacks     |
| 2.5 | CSRF Protection          | Attempt to submit login from external form  | System validates form origin and prevents CSRF attacks         |

### 3. Rate Limiting and Anti-Automation

| #   | Test Description             | Test Steps                                         | Expected Behavior                                              |
| --- | ---------------------------- | -------------------------------------------------- | -------------------------------------------------------------- |
| 3.1 | IP-Based Rate Limiting       | Make multiple rapid login attempts from same IP    | System limits excessive login attempts with appropriate delays |
| 3.2 | CAPTCHA/reCAPTCHA Triggering | Make several failed login attempts                 | CAPTCHA appears after predetermined number of failures         |
| 3.3 | Account-Based Rate Limiting  | Make multiple rapid attempts for same user account | System implements progressive delays for repeated attempts     |
| 3.4 | Brute Force Protection       | Attempt rapid sequential password attempts         | System detects and blocks brute force attempts                 |
| 3.5 | Automated Login Prevention   | Attempt login using automation tools               | System detects and prevents automated login attempts           |

### 4. User Experience and Feedback

| #   | Test Description                  | Test Steps                             | Expected Behavior                                               |
| --- | --------------------------------- | -------------------------------------- | --------------------------------------------------------------- |
| 4.1 | Error Message Security            | Enter invalid credentials              | Generic error message that doesn't specify which field is wrong |
| 4.2 | Remember Me Functionality         | Login with "Remember Me" option        | Session persists appropriately based on user selection          |
| 4.3 | Visual Feedback During Submission | Submit login form and observe          | Loading indicators show submission progress                     |
| 4.4 | Login History/Notification        | Login from new device/location         | User notified of new login if security feature is implemented   |
| 4.5 | Clear Navigation Options          | Check navigation options on login page | Links to registration, password reset clearly available         |

### 6. Session Management

| #   | Test Description     | Test Steps                                   | Expected Behavior                                          |
| --- | -------------------- | -------------------------------------------- | ---------------------------------------------------------- |
| 6.1 | Session Timeout      | Login and leave session inactive             | Session expires after configured timeout period            |
| 6.2 | Concurrent Sessions  | Login from multiple browsers/devices         | Sessions handled based on security policy (allow or limit) |
| 6.3 | Session Revocation   | Login and change password                    | All existing sessions are invalidated on password change   |
| 6.4 | Session Persistence  | Close and reopen browser with active session | Session persists or terminates based on security settings  |
| 6.5 | Logout Functionality | Login and then use logout function           | Session is properly terminated and user is redirected      |

### 7. Edge Cases and Special Situations

| #   | Test Description              | Test Steps                                                       | Expected Behavior                                      |
| --- | ----------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------ |
| 7.1 | Account Status Validation     | Attempt to login to suspended/deactivated account                | System prevents login with appropriate message         |
| 7.2 | Unverified Account Login      | Login to account that hasn't completed email verification        | System handles unverified accounts according to policy |
| 7.3 | Password Expired              | Login to account with expired password                           | User is prompted to update password if policy requires |
| 7.4 | Cross-Browser Compatibility   | Test login on different browsers (Chrome, Firefox, Safari, Edge) | Login works consistently across browsers               |
| 7.5 | Login with Special Characters | Login with credentials containing special characters             | Special characters are handled correctly               |

**Post-conditions:**

- User is successfully authenticated into the system
- Appropriate session is established with proper security controls
- User is directed to correct dashboard/page based on role
- Failed login attempts are properly handled with security measures
- Login is secure against common attack vectors
