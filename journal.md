# Week 1 — Lab Build Journal

**Project:** Mini-SOC in a Box / LabShop  
**Scope:** Week 1 only  
**Reporting note:** The student reported no significant installation or configuration problems. Entries below describe the work and available screenshots; no failure or fix has been fabricated. The evidence is based on the captured lab screenshots.

## Entry 1 — Virtual machines and network design
**Task:** Build the three-machine isolated SOC lab.  
**Actions:** Configured the SIEM host, Ubuntu web endpoint and Windows endpoint, including host-only networking and the required NAT setup.  
**Result:** Network configuration and connectivity tests were documented.  
**Issues encountered:** No significant issues reported.  
**Lessons learned:** The host-only segment separates lab traffic from external networks while allowing endpoint-to-SIEM communication.  
**Evidence:** Screenshots 1–29 and 125–129.

## Entry 2 — Web endpoint and connectivity
**Task:** Prepare the Ubuntu web server.  
**Actions:** Configured SSH, Nginx, web connectivity and HTTP checks.  
**Result:** Nginx service and web-page verification evidence was captured.  
**Issues encountered:** No significant issues reported.  
**Lessons learned:** Verify each network and application layer before introducing telemetry.  
**Evidence:** Screenshots 30–43 and 101–102.

## Entry 3 — Docker and Wazuh deployment
**Task:** Deploy the Wazuh single-node stack on the SIEM host.  
**Actions:** Installed Docker, deployed the stack, reviewed running containers and measured idle memory usage. Documented indexer kernel configuration and dashboard login.  
**Result:** Screenshots show the stack, version-check command and resource checks.  
**Issues encountered:** No significant issues reported.  
**Lessons learned:** Container status, host kernel settings and persistent volumes matter for SIEM reliability.  
**Evidence:** Screenshots 44–64 and 115–120.

## Entry 4 — Endpoint agents and Windows Sysmon
**Task:** Enroll Linux and Windows endpoints.  
**Actions:** Installed/configured Wazuh agents, installed Sysmon and checked telemetry in the dashboard.  
**Result:** Agent and event verification screenshots were captured.  
**Issues encountered:** No significant issues reported.  
**Lessons learned:** Sysmon provides richer process-level Windows telemetry than basic system logs.  
**Evidence:** Screenshots 65–85, 103–110 and 133.

## Entry 5 — Security event verification and recovery checks
**Task:** Generate known events and verify service continuity.  
**Actions:** Investigated SSH authentication failures, sudo, local Linux account creation, Windows logon failure and Sysmon process events; documented stop/start and reboot tests, clock checks, network isolation and snapshots where available.  
**Result:** Event-detail and after-restart screenshots were captured. The five rule IDs and levels are recorded in README.md, and the snapshot screenshots are included.  
**Issues encountered:** No significant issues reported.  
**Lessons learned:** A detection is most useful when supported by an event record, rule description, severity and preserved evidence.  
**Evidence:** Screenshots 86–114 and 121–137.

## Persistence test notes
Screenshots 121, 122a–122c, 123 and 124a–124b are the before/after evidence set for Docker restart and host reboot. Check the agent names and alert counts against those images or the running lab before claiming an exact before/after total.
