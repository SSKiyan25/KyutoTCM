## **SEC-0004:** Authentication Testing - Log in with Google

> **Summary:** Verify that users can successfully log in to the Verch web application using Google OAuth authentication, ensuring proper integration, security, and user experience.

**Preconditions:**

- Tester has access to the Verch web application login page
- Tester has valid Google account(s) that are already registered within the system
- Internet connection is stable
- OAuth integration with Google is properly configured
- Test accounts with various statuses and roles are available (standard, admin, suspended, etc.)

### 1. Basic Google OAuth Login

| #   | Test Description                | Test Steps                                                                 | Expected Behavior                                                   |
| --- | ------------------------------- | -------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| 1.1 | Standard Google Login           | 1. Navigate to login page<br>2. Click "Log in with Google"<br>3. Authorize | User is authenticated and redirected to appropriate dashboard       |
| 1.2 | Google Button UI Elements       | Examine Google login button appearance and placement                       | Button follows Google branding guidelines and is prominently placed |
| 1.3 | Google Authentication Flow      | Initiate Google login and observe flow                                     | User is properly redirected to Google consent screen and back       |
| 1.4 | Login with Different User Types | Test login with different user role accounts linked to Google              | Each user type is directed to appropriate dashboard/section         |
| 1.5 | Accessibility                   | Test Google login using keyboard navigation and screen readers             | Process is fully accessible with proper labels and navigation       |

### 2. Security Measures

| #   | Test Description               | Test Steps                                                    | Expected Behavior                                              |
| --- | ------------------------------ | ------------------------------------------------------------- | -------------------------------------------------------------- |
| 2.1 | OAuth State Parameter          | Monitor request parameters during OAuth flow                  | State parameter is used to prevent CSRF in OAuth flow          |
| 2.2 | Token Validation               | If possible, check token validation process                   | Google tokens are properly validated before accepting          |
| 2.3 | Session Security               | Login with Google and examine session tokens/cookies          | Secure, HTTPOnly flags set on session cookies when appropriate |
| 2.4 | Login with Unregistered Google | Attempt to login with Google account not registered in system | System provides clear message that account doesn't exist       |
| 2.5 | OAuth Error Handling           | Cancel Google authorization or simulate errors                | System handles OAuth errors gracefully with clear messages     |

### 3. Rate Limiting and Anti-Automation

| #   | Test Description               | Test Steps                                                    | Expected Behavior                                                |
| --- | ------------------------------ | ------------------------------------------------------------- | ---------------------------------------------------------------- |
| 3.1 | IP-Based Rate Limiting         | Make multiple rapid Google login attempts from same IP        | System limits excessive login attempts                           |
| 3.2 | Account-Based Monitoring       | Make multiple Google login attempts for same account          | System implements appropriate monitoring for suspicious activity |
| 3.3 | OAuth Redirect Validation      | Attempt to manipulate OAuth redirect parameters               | System validates OAuth redirect parameters for security          |
| 3.4 | Google API Quota Consideration | Test large number of logins (if possible in test environment) | System handles API quota limitations appropriately               |
| 3.5 | Automated Login Prevention     | Attempt automated Google logins using scripts (if applicable) | System detects and prevents automated login attempts             |

### 4. User Experience and Feedback

| #   | Test Description               | Test Steps                                       | Expected Behavior                                               |
| --- | ------------------------------ | ------------------------------------------------ | --------------------------------------------------------------- |
| 4.1 | Login Success Feedback         | Complete successful Google login                 | User receives clear indication of successful authentication     |
| 4.2 | Error Message Clarity          | Trigger various error conditions in Google login | Error messages are clear, specific, and actionable              |
| 4.3 | Visual Feedback During Process | Initiate Google login and observe                | Loading indicators show login progress at each stage            |
| 4.4 | Login History/Notification     | Login from new device/location                   | User notified of new login if security feature is implemented   |
| 4.5 | Google Account Selection       | Test with multiple Google accounts in browser    | Google account selector displays correctly if multiple accounts |

### 5. Session Management

| #   | Test Description     | Test Steps                                                    | Expected Behavior                                            |
| --- | -------------------- | ------------------------------------------------------------- | ------------------------------------------------------------ |
| 5.1 | Session Timeout      | Login with Google and leave session inactive                  | Session expires after configured timeout period              |
| 5.2 | Concurrent Sessions  | Login with Google from multiple browsers/devices              | Sessions handled based on security policy (allow or limit)   |
| 5.3 | Session Persistence  | Close and reopen browser with active Google login session     | Session persists or terminates based on security settings    |
| 5.4 | Logout Functionality | Login with Google and then use logout function                | Session is properly terminated and user is redirected        |
| 5.5 | Google Token Refresh | Maintain session for extended period to trigger token refresh | Session maintains integrity when Google tokens are refreshed |

### 6. Account Status Validation

| #   | Test Description                  | Test Steps                                                         | Expected Behavior                                          |
| --- | --------------------------------- | ------------------------------------------------------------------ | ---------------------------------------------------------- |
| 6.1 | Suspended Account Login           | Attempt to login with Google to a suspended account                | System prevents login with appropriate message             |
| 6.2 | Deactivated Account Login         | Attempt to login with Google to a deactivated account              | System prevents login with appropriate message             |
| 6.3 | Account Requiring Additional Auth | Login to account requiring additional authentication beyond Google | System properly enforces additional authentication steps   |
| 6.4 | Password Change Effect            | Change password for user with Google login enabled                 | Google login continues to function despite password change |
| 6.5 | Account Status Changes            | Login with Google before and after account status changes          | System correctly enforces account status restrictions      |

### 7. Edge Cases and Integrations

| #   | Test Description            | Test Steps                                                              | Expected Behavior                                             |
| --- | --------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------- |
| 7.1 | Cross-Browser Compatibility | Test Google login on different browsers (Chrome, Firefox, Safari, Edge) | Google login works consistently across browsers               |
| 7.2 | Mobile Device Compatibility | Test Google login on mobile devices/responsive views                    | Process works correctly on mobile devices and small screens   |
| 7.3 | Network Interruption        | Interrupt network during Google login process                           | System handles interruptions gracefully with recovery options |
| 7.4 | MFA Integration             | Test Google login for account with MFA enabled                          | MFA challenge presented correctly after Google authentication |
| 7.5 | Remember Me Functionality   | Login with Google with "Remember Me" option                             | Session persists appropriately based on user selection        |

**Post-conditions:**

- User is successfully authenticated into the system using Google OAuth
- Appropriate session is established with proper security controls
- User is directed to correct dashboard/page based on role
- Google token is properly validated and securely handled
- Login is secure against common attack vectors
- User experience is smooth and consistent
