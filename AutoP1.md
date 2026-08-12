# Windows Autopilot V1 

## Platforms and Languages Leveraged

- EDR Platform: Microsoft Defender for Endpoint

## What you'll do:
Setup Autopilot V1 and enrol Windows VM 

## Prerequisite Environment Checks:

- Ensure Intune license configured
- Check MDM authority is Intune, this link allow you to set authority...
  
      https://intune.microsoft.com/#view/Microsoft_Intune_Enrollment/ChooseMDMAuthorityBlade/
  
- Device platform restriction





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


