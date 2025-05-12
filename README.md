# CICFlowMeter (V2)

CICFlowMeter (V2) is an open-source tool developed by the Canadian Institute for Cybersecurity for network traffic analysis. It converts PCAP files into CSV format by generating bidirectional flows and extracting time-related statistical features.
## Key Features
- Converts .pcap files to .csv for analysis and machine learning purposes.
- Generates bidirectional network flows with detailed information.
- Computes over 80 traffic features, such as inter-packet timing, transfer rates, entropy, etc.


## System Requirements

- **Java:** Version 8 or 11.
  - Not compatible with Java 17 or higher.
- **Libraries:**  
  - [`jnetpcap`](https://github.com/slytechs/jnetpcap) (including `libjnetpcap.so` for Linux)  
  - [`libpcap`](https://www.tcpdump.org/)


## Installation

### Step 1: Clone the Source Code
bash

```bash
git clone https://github.com/bqmxnh/CICFlowMeter.git
cd CICFlowMeter
```

### Step 2: Install Dependencies
```bash

sudo apt update
sudo apt install libpcap-dev
```
### Step 3: Run the Tool
Ensure the jnetpcap library is in the system library path or specify its location. Run the tool with the following command:
```bash
java -Djava.library.path=/path/to/libjnetpcap -jar path/to/CICFlowMeter.jar ~/path/to/input/ ~/path/to/output/
```
- /path/to/input/: Directory containing .pcap files.
- /path/to/output/: Directory for storing output .csv files.

# References
- CICFlowMeter on GitHub
- jNetPcap
- Canadian Institute for Cybersecurity
