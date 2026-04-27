# rsyslog-centralized-logging
## Project Overview
This project demonstrates a centralized logging architecture using `rsyslog`.
A dedicated log server receives logs from remote Linux clients over TCP and stores them in structured per-host log files for monitoring, auditing, and incident response.

## Why This Project?
In case of any system compromise or issue, the local logs can be lost or tampered with.
So, making a centralized place to hold logs will help in improving visibility, preserving log integrity, and supporting incident investigation.

## The Architecture
<img width="12317" height="5120" alt="github-rsyslog-log" src="https://github.com/user-attachments/assets/b833a7eb-48e4-421e-95b3-239ec49212be" />
