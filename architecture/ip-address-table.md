# Lab network addressing — observed evidence

| Machine | Host-only IP | Permanent NAT | Evidence |
|---|---|---|---|
| siem-host | **192.168.56.10** | Yes | Screenshot 8 and Wazuh dashboard URL in screenshot 114 |
| ubuntu-web | **192.168.56.20** | No | Screenshot 22; `agent.ip` in screenshot 114 |
| win-client | **192.168.56.30** | No | Screenshot 110 (`agent.ip`); screenshot 127 shows host-only adapter |

The lab uses the 192.168.56.0/24 host-only network. The SIEM host also uses NAT to obtain updates.
