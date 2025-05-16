## **ORG-0003:** Organization testing - Verify Organization Email

> **Summary:** Verify that an organization can verify their email by clicking the verification link.

**Preconditions:**

- A new organization has been added to the system.
- Organization has access to the Gmail account used during registration.

Scenario 1

| #   | Step                                                                   | Expected Behavior                               |
| --- | ---------------------------------------------------------------------- | ----------------------------------------------- |
| 1   | Open Gmail account that was used when registering the organization.    | Verify that the Gmail inbox is accessible.      |
| 2   | Find and open the email from KyutoTCM about organization verification. | Verify that the verification email is received. |
| 3   | Click on the verification link in the email.                           | Verify that clicking the link is successful.    |

**Post-conditions:**

- The organization's email is verified in the system.
