# Linux Security Log Investigation Report

## Executive Summary

A Linux system log investigation was conducted using Splunk Cloud to identify potentially suspicious activity.

The analysis focused on identifying unusual network connections and reviewing FTP-related events.

## Data Source

- Linux system logs
- Splunk Cloud SIEM platform

## Investigation Findings

During analysis, a single external IP address was identified as generating repeated FTP connection attempts.

Source IP:

`211.107.232.1`

Total Events:

`22 FTP connection attempts`

Service:

`ftpd`

## Analysis

The connection attempts occurred within a short timeframe, creating a burst pattern of activity.

The repeated nature of these connections may indicate:

- Automated scanning
- Reconnaissance activity
- Attempted unauthorized access

However, based on the available logs, there was not enough information to confirm whether authentication attempts or successful compromise occurred.

## Risk Assessment

Severity: Medium

Reason:

The activity represents unusual external interaction with an FTP service. Further investigation would be required to determine intent and impact.

## Recommended Actions

- Review authentication logs for related login attempts
- Perform IP reputation analysis
- Monitor future activity from the source IP
- Disable unnecessary FTP services if applicable
- Implement additional access controls

## Conclusion

This investigation demonstrates the process of using Splunk Cloud to ingest logs, identify suspicious behavior, extract relevant information, and document security findings.
