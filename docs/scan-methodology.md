# Nmap Scan Methodology

## Objective

Explore Nmap in a controlled local environment and document observed TCP port and service information.

## Authorized Target

`127.0.0.1` (localhost), the local computer.

## Command

    nmap -sV -sT -Pn 127.0.0.1

- `-sV`: attempts service and version detection.
- `-sT`: performs a TCP connect scan.
- `-Pn`: skips host discovery and treats the target as online.

## Procedure

1. Verify that Nmap is installed.
2. Run the scan against localhost.
3. Review port states and detected services.
4. Record only observations supported by the scan output.

## Observed Results

**Target:** `127.0.0.1` (localhost)

**Scan type:** TCP connect scan with service-version detection

**Host status:** Up

**Open TCP ports observed:** 5

| Port | State | Service detected |
|---|---|---|
| 135/tcp | Open | Microsoft Windows RPC |
| 445/tcp | Open | Microsoft-DS; exact service identification uncertain |
| 903/tcp | Open | VMware Authentication Daemon 1.10 |
| 3306/tcp | Open | MySQL 8.0.45 |
| 5357/tcp | Open | Microsoft HTTPAPI 2.0 |

Nmap reported 995 other scanned TCP ports as closed.

## Interpretation

An open port indicates that a service responded to a local connection attempt. It does not, by itself, prove that the service is vulnerable or reachable from another device.

The results are Nmap's service identifications and have not independently verified each service configuration.

## Recommended Follow-up

- Confirm that each detected service is expected and needed.
- Review relevant service configurations and Windows Firewall rules.
- Check whether the database and VMware services need to be running.
- Do not disable services without understanding their purpose.
- Perform additional testing only on systems and networks for which authorization is available.

## Limitations

This scan targeted localhost. It does not establish external network exposure, identify every possible vulnerability, or guarantee that all service-version detections are accurate.
