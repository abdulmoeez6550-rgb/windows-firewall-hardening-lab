# Windows Firewall Hardening & Access Control Lab

**Cybersecurity Internship Project — Spurvance Labs**

## Project Overview

This project demonstrates the configuration and testing of Windows Defender Firewall inbound access controls.

## Objectives

- Verify the default-deny policy for unmatched inbound connections.
- Create inbound allow rules for TCP ports 22, 80, and 443.
- Create an explicit block rule for TCP port 9999.
- Test inbound connectivity from another device on the local network.
- Document the configuration and test results.

## Lab Environment

- Operating System: Windows 11
- Firewall: Windows Defender Firewall with Advanced Security
- Test Server: Node.js TCP listeners
- Test Client: Android phone using Chrome and PortDroid
- Network: Local Wi-Fi

## Firewall Configuration

| TCP Port | Purpose | Action |
|---|---|---|
| 22 | SSH | Allow |
| 80 | HTTP | Allow |
| 443 | HTTPS | Allow |
| 9999 | Test port | Block |

The lab rules were scoped to the local subnet. Existing application firewall exceptions were left unchanged.

## Test Results

The Android port scan detected:

- TCP 22: Open
- TCP 80: Open
- TCP 443: Open
- TCP 9999: Not accessible

These results demonstrate TCP connectivity and filtering behavior. The temporary listeners were not actual SSH or HTTPS services.

## Security Considerations

The configuration was tested in a controlled local network. Temporary test listeners and firewall rules should be removed after the lab.

## Documentation

See the assignment PDF and screenshots in this repository for configuration details and supporting evidence.
