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
  
- Intune - Devices - Enrollment - Device Platform Restriction - Create restriction

<img width="1212" alt="image" src="AP2.png">

- Name restriction 

<img width="1212" alt="image" src="AP3.png">

- Block personally owned devices

<img width="1212" alt="image" src="AP4.png">

- Scope tags

<img width="1212" alt="image" src="AP5.png">

- Assign to all users

<img width="1212" alt="image" src="AP6.png">

- Create restriction

<img width="1212" alt="image" src="AP7.png">

- New restriction becomes priority

<img width="1212" alt="image" src="AP8.png">

---

## Windows Autopilot V1

1. Capture and save hardware hash 

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
2. In Intune Devices - Enrollment - Devices - Import the hash.csv file
<img width="1212" alt="image" src="apa1.png">
3. Device will appear
<img width="1212" alt="image" src="apa2.png">
4. Assign user to the device
<img width="1212" alt="image" src="apa3.png">
5. Create deployment profile, Device - Enrollment - Windows Autopilot Deployment profiles - Create Profiles - Windows PC, name the profile
<img width="1212" alt="image" src="apa4.png">
6. Configure OOBE, device name template added in this example
<img width="1212" alt="image" src="apa5.png">
7. Assign to all devices
<img width="1212" alt="image" src="apa6.png">
8. Create profile
<img width="1212" alt="image" src="apa7.png">
9. Create an app, Apps - Windows - Create (MS 365 Apps in example)
<img width="1212" alt="image" src="apa8.png">
10. Configure app information
<img width="1212" alt="image" src="apa9.png">
11. Configure app suite
<img width="1212" alt="image" src="apa10.png">
12. Add to all devices
<img width="1212" alt="image" src="apa11.png">
13. Create app
<img width="1212" alt="image" src="apa12.png">
14. Reset Windows VM
<img width="1212" alt="image" src="ps2.png">
15. User automatically assigned to device, enter password 
<img width="1212" alt="image" src="ps3.png">
16. Device setup with name and MS 365 apps installed
<img width="1212" alt="image" src="ps4.png">



