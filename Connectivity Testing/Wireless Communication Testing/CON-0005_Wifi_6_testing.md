## **CON-0005:** Connectivity Testing - WiFi 6 (802.11ax)

> **Summary:** Verify that the KyutoTCM application leverages the benefits of WiFi 6 (802.11ax) including higher data rates, improved performance in dense environments, and better power efficiency, following the design guidelines in https://github.com/SSKiyan25/kyuto.

**Preconditions:**

- Tester has access to the Verch application
- Tester has access to WiFi 6 compatible devices and WiFi 6 router
- Tester has appropriate permissions to access all application sections
- Testing environment includes both WiFi 6 and older WiFi standards for comparison

### 1. Basic WiFi 6 Performance

| #   | Test Description                | Test Steps                                                | Expected Behavior                                       |
| --- | ------------------------------- | --------------------------------------------------------- | ------------------------------------------------------- |
| 1.1 | Application Launch on WiFi 6    | 1. Connect to WiFi 6 network<br>2. Launch app             | App loads within 3-5 seconds with loading indicators    |
| 1.2 | Comparative Launch Performance  | 1. Launch app on WiFi 6<br>2. Launch on WiFi 5 (802.11ac) | WiFi 6 shows 15-25% faster loading times on average     |
| 1.3 | Dashboard Performance           | Navigate to dashboard on WiFi 6                           | Dashboard loads completely within 2-4 seconds           |
| 1.4 | Application Stability on WiFi 6 | Use app for extended period (30+ min) on WiFi 6           | App maintains stable connection without disconnects     |
| 1.5 | Signal Range Testing            | Test app at various distances from WiFi 6 router          | Maintains connectivity at greater distances than WiFi 5 |

### 2. Dense Environment Performance

| #   | Test Description                         | Test Steps                                                          | Expected Behavior                                           |
| --- | ---------------------------------------- | ------------------------------------------------------------------- | ----------------------------------------------------------- |
| 2.1 | Multiple Device Performance              | Connect 10+ devices to same WiFi 6 network while using app          | App maintains consistent performance despite device density |
| 2.2 | Congested Environment Testing            | Test in environment with multiple WiFi 6 and other devices active   | Performance degrades less than on previous WiFi standards   |
| 2.3 | High-Traffic Period Performance          | Use app during peak network usage times                             | Maintains reasonable performance with minimal slowdowns     |
| 2.4 | Comparison with WiFi 5 in Dense Settings | Compare performance on WiFi 6 vs WiFi 5 with many connected devices | WiFi 6 shows 20-30% better response times in dense settings |
| 2.5 | Public WiFi 6 Testing                    | Test on public WiFi 6 networks (if available)                       | App functions reliably in shared WiFi 6 environments        |

### 3. Enhanced Throughput & Bandwidth Utilization

| #   | Test Description                | Test Steps                                                    | Expected Behavior                                              |
| --- | ------------------------------- | ------------------------------------------------------------- | -------------------------------------------------------------- |
| 3.1 | Large Dataset Import            | Import large product catalog (500+ items) on WiFi 6           | Import completes within 15-25 seconds with progress tracking   |
| 3.2 | Media-Rich Content Loading      | Load pages with multiple high-resolution images/videos        | Media content loads within 2-4 seconds with smooth progression |
| 3.3 | Bulk Upload Performance         | Upload multiple large files (images/documents) simultaneously | Multiple uploads complete within 10-20 seconds                 |
| 3.4 | High-Definition Video Streaming | Stream product demonstration videos in highest quality        | Videos start within 1-3 seconds with minimal buffering         |
| 3.5 | Multi-Tab Operation             | Open and use multiple instances of app simultaneously         | All instances operate smoothly with minimal interference       |

### 4. Low Latency Operations

| #   | Test Description               | Test Steps                                                   | Expected Behavior                                            |
| --- | ------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 4.1 | Real-time Data Updates         | Monitor live inventory/order updates on WiFi 6               | Updates appear within 1-2 seconds of being made              |
| 4.2 | Interactive Dashboard Response | Interact with complex, data-heavy dashboards                 | Dashboard controls respond within 1 second of interaction    |
| 4.3 | Search & Filter Operations     | Perform complex searches on large datasets                   | Search results appear within 1-3 seconds                     |
| 4.4 | Collaborative Editing          | Test multi-user editing features on WiFi 6                   | Changes sync to other users within 1-2 seconds               |
| 4.5 | Latency Comparison             | Compare response times between WiFi 6 and previous standards | WiFi 6 shows 30-40% lower latency for interactive operations |

### 5. Advanced WiFi 6 Features Utilization

| #   | Test Description                        | Test Steps                                                      | Expected Behavior                                              |
| --- | --------------------------------------- | --------------------------------------------------------------- | -------------------------------------------------------------- |
| 5.1 | OFDMA Resource Allocation               | Monitor app performance during multiple simultaneous operations | Operations complete with minimal interference                  |
| 5.2 | Multi-user MIMO Benefits                | Test with multiple users accessing different app sections       | All users experience responsive performance                    |
| 5.3 | BSS Coloring Advantage                  | Test in environment with overlapping WiFi networks              | App shows resilience to interference from neighboring networks |
| 5.4 | TWT (Target Wake Time) Power Efficiency | Monitor device battery consumption over extended app usage      | Lower battery consumption compared to older WiFi standards     |
| 5.5 | 1024-QAM Throughput Benefits            | Transfer large files in ideal signal conditions                 | Achieves higher throughput when signal conditions allow        |

### 6. Network Transition & Mixed Environment Handling

| #   | Test Description                | Test Steps                                               | Expected Behavior                                             |
| --- | ------------------------------- | -------------------------------------------------------- | ------------------------------------------------------------- |
| 6.1 | WiFi 6 to Cellular Transition   | Switch from WiFi 6 to cellular data during active usage  | App transitions smoothly within 2-4 seconds without data loss |
| 6.2 | WiFi 6 to Older WiFi Standards  | Move from WiFi 6 coverage to WiFi 5/4 coverage areas     | App adapts to available bandwidth without disruption          |
| 6.3 | Mixed Device Environment        | Test on networks with mix of WiFi 6 and older devices    | App functions optimally based on device capabilities          |
| 6.4 | Router Firmware Update Handling | Test during/after WiFi 6 router firmware updates         | App reconnects properly after router updates complete         |
| 6.5 | Band Switching (2.4GHz vs 5GHz) | Test performance as device switches between WiFi 6 bands | App maintains functionality during band transitions           |

### 7. Security & Performance Balance

| #   | Test Description                   | Test Steps                                                         | Expected Behavior                                             |
| --- | ---------------------------------- | ------------------------------------------------------------------ | ------------------------------------------------------------- |
| 7.1 | WPA3 Security Protocol             | Test app on WiFi 6 networks with WPA3 security                     | App functions properly with enhanced security protocols       |
| 7.2 | VPN Performance on WiFi 6          | Use app through VPN connection on WiFi 6                           | VPN overhead has minimal impact on performance                |
| 7.3 | Encrypted Traffic Handling         | Monitor performance with fully encrypted connections               | Encryption overhead has minimal impact on user experience     |
| 7.4 | Enterprise WiFi 6 Compatibility    | Test on enterprise WiFi 6 networks with authentication             | App properly handles enterprise authentication requirements   |
| 7.5 | Public Hotspot vs. Private Network | Compare performance on public WiFi 6 hotspots vs. private networks | App maintains security while adapting to network environments |

**Post-conditions:**

- Application performs optimally on WiFi 6 networks
- App takes advantage of WiFi 6 benefits for improved user experience
- Application handles transitions between WiFi standards gracefully
- Battery consumption is optimized when using WiFi 6 features
- Security is maintained without compromising performance
- App remains functional in mixed WiFi environments
