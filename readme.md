# NetworkTool

A simple network tool that sends TCP SYN packets with arbitrary SRC/DST ports and checks for responses.

## Usage

Python and scapy are required.  
To install (run as administrator on Windows):

```sh
pip install scapy
```

### Command Example

```sh
python main.py --dst <destination IP or hostname> --dport <destination port> [--sport <source port>] [--count <number of packets>]
```

```sh
sudo -E $(which python3) main.py --dst <destination IP or hostname> --dport <destination port> [--sport <source port>] [--count <number of packets>]
```

- `--dst`: Destination IP address or hostname (required)
- `--dport`: Destination port number (required)
- `--sport`: Source port number (optional, random if omitted)
- `--count`: Number of packets to send (default: 1)

#### Example

```sh
python main.py --dst 192.168.1.1 --dport 80 --count 5
```

## Notes

- Administrator (or root) privileges may be required.
- Use in accordance with your network environment and security policies.

---

This tool is intended for educational and testing purposes.