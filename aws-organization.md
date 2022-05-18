
## AWS ORGANIZATION

AWS Organizations helps you centrally manage and govern your environment as you grow and scale your AWS resources. Using AWS Organizations, you can create accounts and allocate resources, group accounts to organize your workflows, apply policies for governance, and simplify billing by using a single payment method for all of your accounts.

# AWS Organizations includes

* Manangement or master account
* Memmber accounts 

# Steps invoved in creating an AWS Organization

* The management account creates the organization.

* Search AWS organization on the master account and create an organization

![image](https://user-images.githubusercontent.com/71001536/168986715-c787b206-4365-4300-b05a-b20ef9147316.png)


![image](https://user-images.githubusercontent.com/71001536/168983020-0732cbf2-0b27-4a23-baba-05c6383d305b.png)

* An invite can be sent to an existing accont or a new account 

* An invitation is sent to the member account

* An existing account can be invited using account ID or email 

![image](https://user-images.githubusercontent.com/71001536/168984164-f1cd2689-0e66-4313-97a8-86036fe68c28.png)

* A new accout to be created, can only be invite using email 

![image](https://user-images.githubusercontent.com/71001536/168983665-30c6c7ac-5833-4a0e-9786-682617a18d7d.png)

* Grant *OrganizationAccountAccessRole* to the master account from the member account IAM for trusted entity and permission.

![image](https://user-images.githubusercontent.com/71001536/168991192-aa4e0a5e-4816-490c-8d37-02d8b013e6c9.png)

## If you create a new account the role is automatically given, BUT adding an existing account requires to manually create the role

* The account ID of the master account is given the trusted entity 

![image](https://user-images.githubusercontent.com/71001536/168991466-73b8ed6e-07fe-467a-8686-dc23d454be81.png)

* Attach *AdministratorAccess* permission to the *OrganizationAccountAccessRole*

![image](https://user-images.githubusercontent.com/71001536/168994398-33527ec1-9de4-4652-a76c-1c2183a1a286.png)

![image](https://user-images.githubusercontent.com/71001536/168994958-2fb93d47-efff-4eed-8a8c-3b97dbe6c1fb.png)

* Proceed to Master account and switch role 

![image](https://user-images.githubusercontent.com/71001536/168997096-8ee68b6c-021b-4772-b30b-ee368466c877.png)

* Click on the *Switch role*

![image](https://user-images.githubusercontent.com/71001536/168997340-f3f2d832-b5d1-41a9-9418-ce2ffc044cc3.png)

* Input the account ID, role(*OrganizationAccountAccessRole*) of the member account, then click the *switch role*

![image](https://user-images.githubusercontent.com/71001536/168997677-6d4bb1f3-ded3-4c6d-a831-1ee10b15cd7b.png)

![image](https://user-images.githubusercontent.com/71001536/168999337-d671c0f0-40b6-4e08-a336-6d8fc23c476d.png)



## HIERACCHY STRUCTURE

This enable to create the OU(Organizational Unit) within the root container of the organization. Members account can be grouped into the OU

* In the AWS Organization Dashboard (Master Account), tick the root as specified , then click *actions*

![image](https://user-images.githubusercontent.com/71001536/169041262-1e625fcb-ceb4-4b52-a9fb-f20fbd471c4e.png)

![image](https://user-images.githubusercontent.com/71001536/169041632-bc83bf7e-c024-43bf-a028-c80af470a576.png)

* Click the member account , then click on actions to move 

![image](https://user-images.githubusercontent.com/71001536/169042246-e0a65002-3309-4d3e-9433-67382af740c3.png)

![image](https://user-images.githubusercontent.com/71001536/169042565-76b1e846-7835-42f1-9c46-c6f57ccbd8d1.png)

![image](https://user-images.githubusercontent.com/71001536/169050610-d53d733f-0056-4881-99ff-d80d968f324f.png)







