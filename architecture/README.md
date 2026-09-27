# Lab Architecture

## Components

| Component | Role |
|---|---|
| Kali Linux | Controlled security-testing source |
| Windows 10 | Monitored endpoint |
| Sysmon | Endpoint telemetry |
| Log Forwarder | Sends selected Windows telemetry |
| Ubuntu Server | Splunk SIEM |

## Telemetry Flow

`Kali → Windows 10 → Sysmon / Windows telemetry → Forwarder → Splunk`

Network and endpoint activity is then searched and investigated in Splunk.

## Design Goal

The architecture is intentionally small so that each stage can be traced:

1. Generate activity.
2. Confirm the endpoint records it.
3. Confirm telemetry reaches Splunk.
4. Write or test an SPL detection.
5. Investigate the returned events.
6. Record the result and any visibility gaps.
