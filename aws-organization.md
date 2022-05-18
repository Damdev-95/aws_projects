
## AWS ORGANIZATION

* Using AWS organization to manage account, proper admininstration, consolidated billing, service control policy 

* Manangement or master account
* Memmber accounts 

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





