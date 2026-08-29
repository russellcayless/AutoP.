# Windows Autopilot V1 

## Platforms and Languages Leveraged

- EDR Platform: Microsoft Defender for Endpoint

## What you'll do:
Setup Autopilot V1 and enrol Windows VM 

## Prerequisite Environment Checks:

- Ensure Intune license configured
- Check MDM authority is Intune, this link allow you to set authority...
  
      https://intune.microsoft.com/#view/Microsoft_Intune_Enrollment/ChooseMDMAuthorityBlade/

<img width="1212" alt="image" src="AP1.png">
  
- Device platform restriction

<img width="1212" alt="image" src="AP2.png">
<img width="1212" alt="image" src="AP3.png">
<img width="1212" alt="image" src="AP4.png">
<img width="1212" alt="image" src="AP5.png">
<img width="1212" alt="image" src="AP6.png">
<img width="1212" alt="image" src="AP7.png">
<img width="1212" alt="image" src="AP8.png">

---

Capture and save hardware hash 

```
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
New-Item -Type Directory -Path "C:\HWID"
Set-Location -Path "C:\HWID"
$env:Path += ";C:\Program Files\WindowsPowerShell\Scripts"
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
Install-Script -Name Get-WindowsAutopilotInfo
Get-WindowsAutopilotInfo -OutputFile AutopilotHWID.csv
```


<img width="1212" alt="image" src="ps.png">
<img width="1212" alt="image" src="apa1.png">
<img width="1212" alt="image" src="apa2.png">
<img width="1212" alt="image" src="apa3.png">
<img width="1212" alt="image" src="apa4.png">
<img width="1212" alt="image" src="apa5.png">
<img width="1212" alt="image" src="apa6.png">
<img width="1212" alt="image" src="apa7.png">
<img width="1212" alt="image" src="apa8.png">
<img width="1212" alt="image" src="apa9.png">
<img width="1212" alt="image" src="apa10.png">
<img width="1212" alt="image" src="apa11.png">
<img width="1212" alt="image" src="apa12.png">
<img width="1212" alt="image" src="ps1.png">
<img width="1212" alt="image" src="ps2.png">
<img width="1212" alt="image" src="ps3.png">


