# PCAP IP Address Modifier

## Description
This Python script allows users to replace a specific IP address in a PCAP (Packet CAPture) file with another IP address. It's particularly useful in network analysis and forensics, allowing analysts to modify network traffic data for testing or anonymization purposes.

## Requirements
- Python 3
- Scapy library

To install Scapy, run:

```
pip install scapy
```


## Usage
The script `main.py` can be used as follows:

```
# Replace '192.168.1.100' with '10.0.0.100' in 'input.pcap' and save as 'output.pcap'
replace_ip_in_pcap("input.pcap", "output.pcap", "192.168.1.100", "10.0.0.100")
```

## Functionality

The script performs the following actions:

- Reads the input PCAP file.
- Iterates through each packet, checking for the presence of the original IP address.
- If the original IP is found in either the source or destination field, it is replaced with the new IP.
- The IP (and if necessary, TCP/UDP) checksums are recalculated to maintain packet integrity.
- The modified packets are written to a new PCAP file.

## Disclaimer

    Modifying PCAP files can potentially corrupt the data if not done carefully. Always keep backups of the original files.
    This tool is intended for legal and ethical use only. The user is responsible for adhering to applicable laws and regulations.