## **CON-0001:** Connectivity Testing - 2G/3G Networks

> **Summary:** Verify that the KyutoTCM application functions correctly under 2G and 3G network conditions with limited bandwidth, higher latency, and potential instability, following the design guidelines in https://github.com/SSKiyan25/kyuto.

**Preconditions:**

- Tester has access to the Verch application
- Tester has a mobile device with 2G/3G network capabilities or network throttling tools
- Tester has appropriate permissions to access all application sections

### 1. Initial Load Performance on 2G/3G

| #   | Test Description         | Test Steps                                            | Expected Behavior                                              |
| --- | ------------------------ | ----------------------------------------------------- | -------------------------------------------------------------- |
| 1.1 | Application Launch on 2G | 1. Set device/emulator to 2G network<br>2. Launch app | App loads with reasonable timeout (within 20s) and displays UI |
| 1.2 | Application Launch on 3G | 1. Set device/emulator to 3G network<br>2. Launch app | App loads with reasonable timeout (within 10s) and displays UI |
| 1.3 | Login Page Load on 2G    | 1. Set device to 2G<br>2. Navigate to login page      | Login page loads with placeholder images while loading assets  |
| 1.4 | Login Page Load on 3G    | 1. Set device to 3G<br>2. Navigate to login page      | Login page loads with placeholder images while loading assets  |
| 1.5 | Loading State Visibility | Load app pages under 2G/3G conditions                 | Loading indicators display during content loading operations   |

### 2. Authentication Under Poor Connectivity

| #   | Test Description                         | Test Steps                                              | Expected Behavior                                                |
| --- | ---------------------------------------- | ------------------------------------------------------- | ---------------------------------------------------------------- |
| 2.1 | Login on 2G Network                      | Perform login with valid credentials on 2G network      | Login completes successfully with appropriate loading indicators |
| 2.2 | Login Timeout Handling                   | Initiate login and disconnect network before completion | Error message appears after timeout with retry option            |
| 2.3 | Login on Network Fluctuation             | Login while toggling between online/offline state       | Login either completes or fails gracefully with clear message    |
| 2.4 | Session Persistence on Poor Connectivity | Log in, close app, reopen under poor connectivity       | Session persists and doesn't require re-authentication           |
| 2.5 | Token Refresh on Poor Connectivity       | Wait for auth token to near expiry on poor connection   | Token refreshes successfully or graceful session extension       |

### 3. Critical Feature Functionality on 2G/3G

| #   | Test Description                            | Test Steps                                             | Expected Behavior                                              |
| --- | ------------------------------------------- | ------------------------------------------------------ | -------------------------------------------------------------- |
| 3.1 | Product Listing on 2G Network               | Navigate to product list on 2G network                 | Products load progressively with placeholders for images       |
| 3.2 | Product Detail View on 3G                   | Open product details on 3G network                     | Essential product info loads first, images load progressively  |
| 3.3 | Order Creation on 2G                        | Create new order on 2G network                         | Order creation completes with appropriate progress indication  |
| 3.4 | Inventory Management on 3G                  | Update inventory levels on 3G network                  | Updates complete successfully with progress indicators         |
| 3.5 | Critical Transaction on Network Fluctuation | Submit critical transaction during network fluctuation | Transaction either completes or fails with clear recovery path |

### 4. Data Sync and Offline Capabilities

| #   | Test Description                     | Test Steps                                        | Expected Behavior                                      |
| --- | ------------------------------------ | ------------------------------------------------- | ------------------------------------------------------ |
| 4.1 | Data Synchronization on 2G           | Make changes offline, reconnect to 2G             | Changes sync to server with progress indicator         |
| 4.2 | Partial Content Download             | Download large dataset on 3G                      | Content downloads in chunks with progress indicator    |
| 4.3 | Offline Mode Transition              | Use app while connection drops from 3G to offline | App transitions to offline mode with user notification |
| 4.4 | Resume Failed Operations             | Initiate operation, lose connection, regain on 2G | Operation resumes or offers retry without data loss    |
| 4.5 | Background Sync on Poor Connectivity | Queue multiple changes, connect to poor network   | Changes sync in background with minimal UI blocking    |

### 5. Media and Asset Handling

| #   | Test Description              | Test Steps                                         | Expected Behavior                                              |
| --- | ----------------------------- | -------------------------------------------------- | -------------------------------------------------------------- |
| 5.1 | Image Loading Strategy        | Browse image-heavy screens on 2G                   | Images load progressively with low-res placeholders            |
| 5.2 | Image Upload on 3G            | Upload product images on 3G network                | Upload proceeds with progress indicator and doesn't block UI   |
| 5.3 | Download Asset Optimization   | Download reports/assets on 2G                      | Assets download optimized versions appropriate for connection  |
| 5.4 | Media Cache Utilization       | Browse previously viewed images on poor connection | Previously viewed images load from cache without redownloading |
| 5.5 | Large Media Download Handling | Attempt to download large file on 2G               | App offers optimized version or warns about download size/time |

### 6. Error Handling and Recovery

| #   | Test Description          | Test Steps                                           | Expected Behavior                                                  |
| --- | ------------------------- | ---------------------------------------------------- | ------------------------------------------------------------------ |
| 6.1 | Request Timeout Handling  | Make requests on extremely slow connection           | Requests timeout gracefully with clear error messages              |
| 6.2 | Auto-Retry Strategy       | Observe behavior of failed requests on unstable 2G   | App implements smart retry strategy with backoff                   |
| 6.3 | Partial Response Handling | Force interruption of data transfer on 3G            | App handles partial responses without data corruption              |
| 6.4 | Resumable Operations      | Begin multi-step process, lose connection, reconnect | Operations can be resumed from last successful step                |
| 6.5 | Error Message Clarity     | Trigger connection errors on various operations      | Error messages clearly indicate connectivity issue with next steps |

### 7. Performance and Optimization

| #   | Test Description                  | Test Steps                                             | Expected Behavior                                              |
| --- | --------------------------------- | ------------------------------------------------------ | -------------------------------------------------------------- |
| 7.1 | Payload Size Optimization         | Monitor network traffic on API calls on 2G/3G          | API requests/responses are optimized for size                  |
| 7.2 | Network Request Batching          | Perform multiple operations on 2G                      | Related requests are batched to minimize connections           |
| 7.3 | Resource Prioritization           | Load complex page on 3G                                | Critical resources load first, non-essential deferred          |
| 7.4 | Memory Usage on Poor Connectivity | Use app extensively on 2G with frequent disconnections | App maintains stable memory usage without leaks or crashes     |
| 7.5 | Battery Consumption               | Monitor battery usage during extended 2G/3G use        | App doesn't drain battery excessively during poor connectivity |

**Post-conditions:**

- Application functions acceptably on 2G and 3G network conditions
- Critical operations complete successfully even on poor connectivity
- Appropriate loading indicators and error states are shown
- User data integrity is maintained during connection fluctuations
- Application doesn't crash or freeze during network transitions
- Battery and data usage are optimized for low-bandwidth conditions
