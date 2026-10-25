# Network Scanning with Nmap

A cybersecurity portfolio project exploring network discovery, TCP port scanning, service identification, and security reporting in an authorized lab.

## Objectives

- Understand network reconnaissance.
- Identify open and closed ports.
- Explore service and version detection.
- Document observed results accurately.
- Practice responsible, authorized security testing.

## Tools

- Nmap 7.99
- Windows PowerShell
- Visual Studio Code
- Git and GitHub

## Scan Performed

Verify the installation:

    nmap --version

Scan the local computer:

    nmap -sV -sT -Pn 127.0.0.1

## Observed Results

The localhost scan identified five open TCP ports. See [the scan methodology](docs/scan-methodology.md) for the port table and interpretation.

## Responsible Testing

Only scan systems you own or have explicit permission to test. Review results for sensitive information before sharing them publicly.

## Learning Outcomes

This project demonstrates basic Nmap usage, port and service identification, and documentation of observed scan results.

## Disclaimer

For educational purposes and authorized security testing only.
