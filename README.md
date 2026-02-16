# wifi-signal-analyzer-predictor
A hybrid C and Python-based platform designed to scan, analyze, and predict the most stable Wi-Fi connections in real-time using low-level network data and web-based visualization.

**Optimal Network Prediction System**

**Overview**

The Optimal Network Prediction System is an intelligent network management tool that addresses the challenges of selecting the most stable connection in environments with multiple overlapping Wi-Fi networks. Unlike traditional scanners that only list nearby networks, this system evaluates signal strength, security, and frequency to predict the most reliable connection in real time.

**Key Features**

• Real-Time Network Scanning: Extracts critical parameters including SSID, BSSID, Signal Strength (RSSI), Channel, and Security Type (WPA2/WPA3/Open).
• Intelligent Prediction Algorithm: Automatically recommends the "Best Network" by filtering unstable signals and prioritizing those with optimal performance and encryption.
• Hybrid Backend: Combines the speed of C programming for low-level hardware communication with Python (Flask) for efficient data handling and server management.
• Dynamic Visualization: Includes a web dashboard that provides graphical representations of signal quality and network rankings using Matplotlib.
• Fault Tolerance: Features a backup mechanism using Python’s PyWiFi module to ensure reliability if low-level C scanning encounters hardware permission issues.

**System Architecture**

The project utilizes a modular, multi-layered architecture:
1. Low-Level Backend (C): Executes the Windows utility netsh wlan show networks mode=bssid to gather raw hardware-level data.
2. Middleware (Flask): Serves as a bridge between the C computation core and the frontend via HTTP protocols.
3. Frontend (HTML/CSS/JS): A responsive user interface for monitoring network utilization and viewing analyzed results.
4. Database (MySQL): Handles user authentication and secure data storage.
   
**Technical Implementation Details**

• Signal Normalization: The system converts raw RSSI values into a standardized 0–100% signal quality percentage for easier comparison.
• Protocol Identification: Automatically identifies Wi-Fi protocols (e.g., 802.11b/g/n vs. 802.11ac) based on frequency and channel data.
• Distance Estimation: Computes an approximate distance to access points based on signal degradation.

**Future Enhancements**

• Integration of AI and Machine Learning for improved historical performance tracking and anomaly detection.
• Cloud-based analytics for cross-platform data synchronization
