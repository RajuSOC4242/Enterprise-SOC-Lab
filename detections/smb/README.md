# SMB Activity Detection

## Objective

Monitor SMB-related activity generated during controlled testing and investigate the resulting Windows/SIEM telemetry.

## Test

SMB client activity was generated from the Kali lab host toward the Windows endpoint.

## Detection

Add the validated SPL query here once the exact index, sourcetype and fields have been confirmed.

## Investigation Fields

Capture, where available:

- Timestamp
- Source host / IP
- Destination host / IP
- Username
- Process or service
- Event ID
- Action
- Share/resource
- Result/status

## Validation

Document whether the expected telemetry appeared in Windows and Splunk. If an activity test produces no new event, record that as a visibility gap and investigate the collection path instead of treating the test as a successful detection.
