# Novastar-Novaicare-Privilege-Escalation

Vulnerability Description: The application Novaicare developed by Xi'an NovaStar Tech Co.,Ltd which is used to centrally monitor display status of LED screens suffers from Multiple Privilege Escalation Bugs.The bug lies in the poor access control management for low privileged users on the platform.

Observation: When a new user is created on the Novaicare platform and added to a restricted role( a role with only User view and edit privileges) , that user can escalate the privileges and perform multiple privileged actions including : 1. View Corporate Information and SMTP Server Details 2. Ability to delete Users 3. Ability to view roles .

1. View Enterprise and SMTP Info

Below POC shows the User "Test" account created with restricted role:

<img width="1414" alt="image" src="https://user-images.githubusercontent.com/16098568/128646824-28ae4721-4c9c-4b87-8118-386cb6f05030.png">

Restricted Role Privileges have been shown below:

<img width="1440" alt="image" src="https://user-images.githubusercontent.com/16098568/128646855-7fd71464-1929-4183-b6bd-31842169d36a.png">

As User Test should not be allowed to view Corporate Information and SMTP Server Details but below POC show that user Test was able to view these details by browsing to the specific endpoints thus resulting in privilege escalation:

::Corporate Information::

Visit Endpoint given in POC with a restricted role User account : 

<img width="1278" alt="image" src="https://user-images.githubusercontent.com/16098568/128647130-12d8d848-6977-4afb-a147-3a8494049605.png">

::SMTP Server Details::

Visit Endpoint given in POC with a restricted role User account : 

<img width="1281" alt="image" src="https://user-images.githubusercontent.com/16098568/128647162-9e64edad-f7f2-4a7f-8d95-14cbf2bd2de8.png">









