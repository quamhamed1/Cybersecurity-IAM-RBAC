##Step 1: Setting up the Azure AD Tenant

A new Azure AD Tenant ('RBAC-Lab-Tenant') was created for the purpose of demonstrating RBAC implementation
The domain used by the tenant is 'rbaclab.onmicrosoft.com'


![image](https://github.com/user-attachments/assets/c36ebf44-6f89-4d64-8653-540e2ab5ccf1)

![image](https://github.com/user-attachments/assets/738bada9-0fcb-43fc-b22e-773f31f6bd3b)



##Step 2: Creating users and Groups

In this step, three users and groups were created

    Users                     Groups 

- RBAC Admin 1     --->  RBAC - Readers
- RBAC Contributor 1 --->  RBAC - Admins 
- RBAC Reader User 1 ---> RBAC - Contributors 

![image](https://github.com/user-attachments/assets/8716ad75-d6dd-415b-8791-78595d8d0494)

![image](https://github.com/user-attachments/assets/2455a61e-f2d8-4bbc-8ab7-cc3d88a0878b)


##Step 3: Assigning Users to groups

Newly created Users are added to their associated groups

![image](https://github.com/user-attachments/assets/b5bf8ef8-d562-437e-833e-4fdf0b77b03c)

![image](https://github.com/user-attachments/assets/d247d83d-ee3e-44d6-b1b2-c50a8289d616)

![image](https://github.com/user-attachments/assets/ee30ff46-0f3d-4fbe-8724-547b1d3245a0)


##Step 4: Assigning RBAC Roles to groups

In this step, roles were assigned to the newly created groups. 

***RBAC-Readers ---> assigned Reader role 

![image](https://github.com/user-attachments/assets/d6433c0e-3e82-4d13-9a18-7b7c14ad2142)

![image](https://github.com/user-attachments/assets/a946e682-241c-4cf4-a445-8226db6fc06c)


***RBAC-Contributors --->assigned Contributor role 

![image](https://github.com/user-attachments/assets/f5192cf5-7386-4123-882c-b9ed94a950e0)

![image](https://github.com/user-attachments/assets/a18bec58-a9e0-43ba-acbd-584cd68e870e)

***RBAC-Admins ---> assigned Owner role

![image](https://github.com/user-attachments/assets/37b74553-bdde-4b38-b987-97c75c0de20f)

![image](https://github.com/user-attachments/assets/c9b5ccf6-8894-4d43-8258-a663d869a3f2)

##Step 5: Testing RBAC implementation

During testing, I ensured that the assigned roles worked as expected for different accounts 

**Admin (RBAC-Admins)**: Full access to create, modify, and delete resources 

![image](https://github.com/user-attachments/assets/911c0e2b-cd7c-458a-b0e9-581d45b9af36)

**Contributor Role Validation

- Create Resource: Successfully created a new storage account.

![image](https://github.com/user-attachments/assets/011db076-af87-4fc8-b56d-8ae82bdaef0b)

- Modify Resource: Successfully modified the Secure Transfer setting for the Storage Account.

![image](https://github.com/user-attachments/assets/6763fe66-fcef-4ea7-9070-729a7ef47a4b)

- Manage Access: Failed to manage access, as expected. 

![image](https://github.com/user-attachments/assets/cb44fe38-3adb-4381-8a55-38ecaf909b3a)


**Reader Role Validation 

The reader role was tested for the following actions:
- View resource: Successfully viewed resource details.
- Modify resource: Failed to modify settings, as expected.

  ![image](https://github.com/user-attachments/assets/1755fd3e-663d-4b48-b36c-0a93e01845ef)

- Create resource: Failed to create new resources, as expected.

  ![image](https://github.com/user-attachments/assets/dda0231c-ac47-4818-a553-5a4679235fbb)

- Manage access: Failed to manage access, as expected.

![image](https://github.com/user-attachments/assets/7a4d3942-c180-4e8d-b1da-5c607c08495e)

