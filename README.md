# PRODIGY_CS_05 NetDetective

**NetDetective** is a Python-based packet sniffer and analyzer built using **Scapy**. It captures and displays network packets, providing insights into IP addresses, protocols, ports, and payload data. This tool is designed for educational purposes and to help users understand network traffic and basic packet analysis.

## Features

- Captures network packets in real-time.
- Displays detailed information about captured packets, including:
  - Source and Destination IP addresses
  - Protocol (TCP, UDP, etc.)
  - Source and Destination Ports
  - Raw Payload Data
- Filter packets based on protocols and IP traffic.
- Easy-to-understand output for educational purposes.


## Requirements

- Python 3.x
- Scapy (for packet capturing and analysis)
- Npcap (Windows users) or libpcap (Linux/macOS users)

### Install Dependencies

To get started, you need to install the required Python libraries and packet capture drivers:

1. Install **Scapy**:
   ```bash
   pip install scapy
   ```

2. Install **Npcap** (for Windows users):
   - Download and install Npcap from [Npcap Official Website](https://nmap.org/npcap/).

3. (Optional) Install **libpcap** if you're on Linux or macOS.

## Installation

1. Clone the repository:

   ```bash
   https://github.com/ThwariqAnwar/PRODIGY_CS_05.git
   ```

2. Install dependencies:

3. Run the tool:

   ```bash
   python netdetective.py
   ```

Captured packets will be displayed in the console with relevant details, such as IP addresses, ports, and the protocol used.

## Example Output

```
Packet Captured:
    Source IP: 142.250.193.174
    Destination IP: 192.168.1.2
    Protocol: TCP
    Source Port: 443
    Destination Port: 54470
    Raw Payload: b'\x01\xbb\xd4\xc6\x17\xeb\x03\x14\xd1`\xfb\x96P\x10\x01\x17\xdd\xf1\x00\x00'
```

### Custom Packet Filtering

You can customize the filtering of the packets by modifying the filter string. For example, if you only want to capture TCP packets:

```python
sniff(prn=packet_handler, filter="tcp", store=0)
```

Or, to capture all HTTP traffic:

```python
sniff(prn=packet_handler, filter="tcp port 80", store=0)
```

## Ethical Use Disclaimer

This tool is intended for **educational purposes only**. Make sure you have permission to capture and analyze network traffic before using this tool on any network. Unauthorized use may violate laws and terms of service agreements.
