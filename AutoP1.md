# Build & Use Threat Intelligence in Microsoft Defender

## Platforms and Languages Leveraged

- EDR Platform: Microsoft Defender for Endpoint

## What you'll do:
Find suspicious IPs in your logs → turn them into TI indicators → confirm they're in the table → match them in queries → build an analytics rule.
Naming: name every indicator with MaliciousFlows — the queries below filter on that name.

1. Find suspicious IPs
Port scanners (from VNet/NSG logs) — SrcIp is the attacker:

```kql

// See who is trying to brute force into the cyber range (latest info)
DeviceLogonEvents
| where ActionType == "LogonFailed"
| summarize Count = count() by RemoteIP, ActionType
| order by Count desc

```

<img width="1212" alt="image" src="threat-intel1.png">

```

2. Create the TI indicators
For each IP:
- Go to Threat intelligence → Intel management → + Add TI Object
- Type: IP address
- Value: the bad IP
- Name: include Malicious Activity
- Set confidence and a future Valid until date
- Save

```

<img width="1212" alt="image" src="threat-intel2.png">


<img width="1212" alt="image" src="threat-intel3.png">


<img width="1212" alt="image" src="threat-intel4.png">

<img width="1212" alt="image" src="threat-intel5.png">


