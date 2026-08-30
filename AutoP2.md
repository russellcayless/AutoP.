# Windows Autopilot V2

## Platforms and Languages Leveraged

- EDR Platform: Microsoft Defender for Endpoint

## What you'll do:
Setup Autopilot V2 and enrol Windows VM 

---

1. Create New devices security group within Entra
   
<img width="1212" alt="image" src="ap21.png">

3. Add Intune Provisioning Client as Owner

<img width="1212" alt="image" src="ap22.png">

4. Create a second users security group within Entra

<img width="1212" alt="image" src="ap23.png">

5. Add an owner to the group

<img width="1212" alt="image" src="ap24.png">

6. Add a member to the group

<img width="1212" alt="image" src="ap25.png">

7. Navigate to Intune - Devices - Enrollment - Device preparation policy - Create - User Driven

<img width="1212" alt="image" src="ap26.png">

8. Name the profile

<img width="1212" alt="image" src="ap27.png">

9. Add device security group previously created

<img width="1212" alt="image" src="ap28.png">

10. Configure settings in the profile

<img width="1212" alt="image" src="ap29.png">

11. Add applications

<img width="1212" alt="image" src="ap30.png">

12. Add scope tags

<img width="1212" alt="image" src="ap31.png">

13. Assign the user security group previously created

<img width="1212" alt="image" src="ap32.png">

14. Save the new profile

<img width="1212" alt="image" src="ap33.png">

15. Extract the manufacture, model and serial number from Windows VM in .csv file

<img width="1212" alt="image" src="apqp2.png">

16. Within Intune navigate to Devices - Enrollment - Corporate Device Identifiers - Add - Enter Manually - Set type to Manufacture... and add .csv file.

<img width="1212" alt="image" src="ap34.png">

17. Reset the VM

<img width="1212" alt="image" src="ps2.png">

18. After reset select set up for work or school

<img width="1212" alt="image" src="apq3.png">

19. Login as user

<img width="1212" alt="image" src="apq4.png">

20. Enter user password

<img width="1212" alt="image" src="apq5.png">

21. Setup will begin

<img width="1212" alt="image" src="apq6.png">

22. VM setup and applications installed

<img width="1212" alt="image" src="apqp7.png">
