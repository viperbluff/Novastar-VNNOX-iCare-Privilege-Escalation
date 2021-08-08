# Novastar-Novaicare-Privilege-Escalation

Vulnerability Description: The application Novaicare developed by Xi'an NovaStar Tech Co.,Ltd which is used to centrally monitor display status of LED screens suffers from Multiple Privilege Escalation Bugs.The bug lies in the poor access control management for low privileged users on the platform.

Observation: When a new user is created on the Novaicare platform and added to a restricted role( a role with only User view and edit privileges) , that user can escalate the privileges and perform multiple privileged actions including : 1. View Enterprise and SMTP Info 2. Ability to delete Users 3. Ability to view roles .

1. View Enterprise and SMTP Info

Below POC shows the User "Test" account created with restricted role:

Screenshot 2021-08-09 at 1.33.02 AM<img width="1414" alt="image" src="https://user-images.githubusercontent.com/16098568/128646824-28ae4721-4c9c-4b87-8118-386cb6f05030.png">






