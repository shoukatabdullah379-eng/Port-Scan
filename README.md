# Asynchronous Python Port Scanner

A fast, lightweight TCP port scanner written in Python 3 using `asyncio`.

## Features
- **Asynchronous Execution:** Scans thousands of ports in seconds using standard library `asyncio`.
- **Zero Dependencies:** Built entirely with standard Python libraries.
- **Configurable Concurrency & Timeout:** Easily tune speed vs. reliability depending on network environment.
- **Service Detection:** Automatically resolves common service names (HTTP, SSH, MySQL, etc.).

## Usage

```bash
# Basic scan (default ports 1-1024)
python scanner.py scanme.nmap.org

# Scan a custom port range
python scanner.py 192.168.1.1 -p 1-65535

# High-concurrency scan with custom timeout
python scanner.py 10.0.0.1 -p 1-10000 -c 1000 -t 0.5
```

### Options
- `target`: IP address or domain name.
- `-p`, `--ports`: Range of ports to scan (e.g., `80`, `1-1024`). Default: `1-1024`.
- `-t`, `--timeout`: Connection timeout per port in seconds. Default: `1.0`.
- `-c`, `--concurrency`: Max simultaneous connection attempts. Default: `500`.

## Disclaimer
This tool is intended strictly for authorized security auditing, educational purposes, and network troubleshooting. Scanning targets without prior permission may violate applicable laws.
