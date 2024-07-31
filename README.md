# Minetracker

Minetracker is a tool designed for detecting cryptocurrency miners and analyzing network traffic. This application is developed as part of the Traffic and Monitoring Analysis course in the Cybersecurity Master's program at UPC.

![Dashboard](captures/dashboard.PNG)

## Project Overview

Minetracker focuses on:

- Detecting cryptocurrency miners, even those with minimal CPU usage or those that evade conventional antivirus solutions.
- Analyzing network packets to gather statistical data and detect suspicious activity.

### Existing Resources

Some existing applications and resources for miner detection include:

- Malwarebytes
- Guides on inspecting machine processes

Many current methods rely on having control over the machines for effective miner detection.

## Features

Minetracker is intended for deployment on routers, enabling the monitoring of all outgoing internet connections.

### Packet Sampling and Analysis

Minetracker supports configurable packet sampling, allowing users to set the number of packets to sample, the number of packets per file, and the duration of sampling. The primary goal is to detect traces of cryptocurrency miners.

Through the dashboard, users can analyze network packets for signs of miner activity. Suspicious IP connections to mining pools or traffic indicative of mining can be tracked and investigated further.

![IP Tracking](captures/analyze.PNG)

### IP Tracking

Minetracker can also process external data from other sources by specifying the folder containing the traffic data. This feature is useful for analyzing traffic data collected during previous sampling sessions to identify any miners.

![Traffic analysis](captures/traffic_analysis.PNG)

If a miner is detected, the dashboard provides detailed information about the external IP, including city, region, country, geolocation, and host name. Users can also block these IPs or enable autoblocking mode for detected miners.

![IP info](captures/ip_info.PNG)

### Data Monitoring

The dashboard includes several plots for comprehensive data monitoring:

1. **Quantity of GPU**:
   - Displays the distribution of GPU rates, showing the quantity of GPUs operating at various rates.

2. **Estimation of Hash Velocity**:
   - Estimates hash velocity, showing the mean hash rate (indicated by a red line) and the distribution of data points.

3. **Estimation of Bandwidth Usage**:
   - Estimates bandwidth usage, displaying the mean hash rate, total bandwidth, and data point distribution.

4. **Power Consumption**:
   - Represents power consumption with an estimated value (34W). This is calculated by:

     - **Capturing Mining Traffic**:
       - Monitoring mining traffic to understand the rate at which the system solves computational problems from the miner pool.

     - **Calculating Hash Rate**:
       - Deriving the hash rate from the problem-solving speed, which is key for further calculations.

     - **Reference Table for Devices**:
       - Using a reference table with average power consumption and hash rates of various devices to estimate power consumption.

     - **Estimating Machine Power**:
       - Inferring the power usage patterns of different components and providing an overall view of the system's power consumption.

![Data Monitoring Dashboard](captures/plots.PNG)

