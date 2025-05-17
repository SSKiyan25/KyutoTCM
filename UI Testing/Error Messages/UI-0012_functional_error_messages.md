## **UI-0012:** Functional Error Messages Testing

> **Summary:** Verify that specific error messages for different functional areas of the application are displayed correctly when appropriate conditions are met, according to the design guidelines in https://github.com/SSKiyan25/kyuto.

**Preconditions:**

- Tester has access to the Verch application
- Tester has appropriate permissions to access all application sections

### 1. Authentication Error Messages

| #   | Error Scenario            | Test Steps                                          | Expected Error Message                                                                             |
| --- | ------------------------- | --------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| 1.1 | Invalid Login Credentials | Enter incorrect username/password and attempt login | "Invalid username or password. Please try again."                                                  |
| 1.2 | Account Locked            | Attempt login to locked account                     | "Your account has been locked due to multiple failed attempts. Please contact your administrator." |
| 1.3 | Session Timeout           | Allow session to expire and attempt action          | "Your session has expired. Please log in again to continue."                                       |
| 1.4 | Permission Denied         | Attempt action without required permissions         | "You don't have permission to perform this action."                                                |
| 1.5 | Invalid Token             | Use expired/invalid token for authentication        | "Authentication failed. Please log in again to continue."                                          |

### 2. Product Management Error Messages

| #   | Error Scenario                | Test Steps                                          | Expected Error Message                                               |
| --- | ----------------------------- | --------------------------------------------------- | -------------------------------------------------------------------- |
| 2.1 | Duplicate Product             | Attempt to create product with existing name/SKU    | "A product with this name/SKU already exists."                       |
| 2.2 | Invalid Product Price         | Enter negative or non-numeric price                 | "Product price must be a positive number."                           |
| 2.3 | Missing Required Fields       | Submit product form with missing required fields    | "Please fill out all required fields."                               |
| 2.4 | Delete Product With Inventory | Attempt to delete product with inventory            | "Cannot delete product with existing inventory. Archive it instead." |
| 2.5 | Invalid Image Format          | Upload product image with unsupported format        | "Unsupported image format. Please use JPG, PNG, or GIF."             |
| 2.6 | Maximum Variations Exceeded   | Attempt to add more than allowed product variations | "Maximum number of variations (X) has been reached."                 |

### 3. Inventory Management Error Messages

| #   | Error Scenario               | Test Steps                                       | Expected Error Message                                         |
| --- | ---------------------------- | ------------------------------------------------ | -------------------------------------------------------------- |
| 3.1 | Insufficient Stock           | Attempt to reduce stock below available quantity | "Insufficient stock. Available quantity: X."                   |
| 3.2 | Invalid Stock Quantity       | Enter negative or non-integer stock quantity     | "Stock quantity must be a positive whole number."              |
| 3.3 | Product Not Found            | Scan/enter non-existent product code             | "Product not found. Please check the product code."            |
| 3.4 | Duplicate Batch Number       | Enter already used batch number                  | "Batch number already exists. Please use a unique identifier." |
| 3.5 | Invalid Date Range           | Set expiry date earlier than manufacturing date  | "Expiry date cannot be earlier than manufacturing date."       |
| 3.6 | Maximum Stock Level Exceeded | Attempt to add stock beyond maximum capacity     | "Maximum stock capacity (X) would be exceeded."                |

### 4. Order Processing Error Messages

| #   | Error Scenario                   | Test Steps                                       | Expected Error Message                                           |
| --- | -------------------------------- | ------------------------------------------------ | ---------------------------------------------------------------- |
| 4.1 | Invalid Order Status Transition  | Attempt disallowed order status change           | "Cannot change order status from X to Y."                        |
| 4.2 | Order Cancellation Period Passed | Attempt to cancel order past cancellation period | "Order cannot be cancelled after shipping/processing has begun." |
| 4.3 | Products Unavailable             | Place order for unavailable products             | "The following products are unavailable: [product list]"         |
| 4.4 | Payment Processing Failed        | Process order with invalid payment details       | "Payment processing failed. Please check payment details."       |
| 4.5 | Invalid Discount Code            | Apply expired or invalid discount code           | "Discount code is invalid or has expired."                       |
| 4.6 | Order Modification Restricted    | Attempt to modify processed order                | "Order cannot be modified in its current state."                 |

### 5. User Management Error Messages

| #   | Error Scenario              | Test Steps                                             | Expected Error Message                              |
| --- | --------------------------- | ------------------------------------------------------ | --------------------------------------------------- |
| 5.1 | Duplicate Username/Email    | Create user with existing username/email               | "Username/email is already in use."                 |
| 5.2 | Password Policy Failure     | Set password that doesn't meet complexity requirements | "Password doesn't meet security requirements."      |
| 5.3 | Delete Admin User           | Attempt to delete last admin user                      | "Cannot delete the only admin user."                |
| 5.4 | Self Role Downgrade         | Admin attempts to remove own admin privileges          | "Cannot remove your own administrative privileges." |
| 5.5 | Invalid Email Format        | Enter improperly formatted email address               | "Please enter a valid email address."               |
| 5.6 | Invalid Phone Number Format | Enter improperly formatted phone number                | "Please enter a valid phone number."                |

### 6. Organization Management Error Messages

| #   | Error Scenario                 | Test Steps                                       | Expected Error Message                                    |
| --- | ------------------------------ | ------------------------------------------------ | --------------------------------------------------------- |
| 6.1 | Duplicate Organization         | Create organization with existing name           | "An organization with this name already exists."          |
| 6.2 | Invalid Commission Rate        | Enter commission rate outside allowed range      | "Commission rate must be between X% and Y%."              |
| 6.3 | Delete Organization With Users | Attempt to delete organization with active users | "Cannot delete organization with active users."           |
| 6.4 | Invalid Organization Code      | Enter invalid format for organization code       | "Organization code must follow the format: XXX-###."      |
| 6.5 | Email Verification Required    | Attempt action requiring verified email          | "Organization email must be verified before this action." |
| 6.6 | Missing Tax Information        | Submit organization without required tax info    | "Tax identification information is required."             |

### 7. Settings & Configuration Error Messages

| #   | Error Scenario                | Test Steps                                          | Expected Error Message                                      |
| --- | ----------------------------- | --------------------------------------------------- | ----------------------------------------------------------- |
| 7.1 | Invalid API Key               | Enter invalid API key for integration               | "Invalid API key. Please check and try again."              |
| 7.2 | Connection Test Failed        | Test connection to external service with bad config | "Connection test failed. Please verify settings."           |
| 7.3 | Reserved System Name          | Attempt to use reserved name in configuration       | "This name is reserved for system use."                     |
| 7.4 | Configuration Save Failed     | Attempt to save invalid configuration               | "Failed to save configuration. Please check error details." |
| 7.5 | Database Backup Failure       | Attempt backup with insufficient permissions        | "Database backup failed. Check permissions and disk space." |
| 7.6 | Invalid Email Server Settings | Configure email with incorrect SMTP settings        | "Could not connect to email server. Verify settings."       |

**Post-conditions:**

- All specified error messages display correctly under appropriate conditions
- Error messages accurately reflect the nature of the error
- Error messages provide clear guidance for resolution when applicable
- Error message content follows terminology and style guidelines
- Error messages are presented in a user-friendly, helpful manner
