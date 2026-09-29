# AlienVault OSSIM SIEM Lab

> Status: In Progress

A hands-on security monitoring lab demonstrating centralized Windows event collection, failed-authentication detection, event correlation, alert investigation, and incident documentation using AlienVault OSSIM.

## Project Objectives

- Deploy AlienVault OSSIM in an isolated virtual environment.
- Configure Windows security auditing.
- Forward Windows security events to OSSIM.
- Generate controlled failed-authentication activity.
- Detect and correlate repeated authentication failures.
- Investigate the resulting security alert.
- Document findings and recommended remediation.

## Planned Lab Environment

| Component | Purpose |
|---|---|
| AlienVault OSSIM | SIEM, event collection, correlation, and alerting |
| Windows Server | Monitored endpoint and authentication target |
| Kali Linux | Authorized security-testing system |
| VirtualBox | Virtualization and isolated lab networking |

## Planned Detection Scenario

The lab will test whether OSSIM can identify multiple failed authentication attempts against a Windows system.

The final detection logic, event threshold, timestamps, source addresses, findings, and response actions will be documented only after the test is completed.

## Planned Documentation

- Network architecture
- Installation and configuration guide
- Windows auditing configuration
- Event-forwarding configuration
- Detection and correlation logic
- Sanitized evidence
- Incident investigation report
- Lessons learned

## Safety and Authorization

All activity will be performed against personally owned virtual machines on an isolated lab network. No testing will target public systems or systems belonging to another person or organization.

## Current Status

- [ ] Verify host system resources
- [ ] Create isolated virtual network
- [ ] Deploy AlienVault OSSIM
- [ ] Deploy Windows Server
- [ ] Deploy Kali Linux
- [ ] Configure Windows event collection
- [ ] Validate event ingestion
- [ ] Run controlled authentication test
- [ ] Create and validate detection logic
- [ ] Complete incident investigation
- [ ] Add sanitized evidence
- [ ] Finalize portfolio documentation
