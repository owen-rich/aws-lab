# AWS: IAM Implementation

## Lab Mission
Learn how to implement IAM features for AWS accounts to provide experience and a better understanding of the IAM concept.


## Resources
- **Environment & Tools**
  - Web browser
- **External Lab Links**
  - [AWS documentation](https://docs.aws.amazon.com/)

## Lab Task 1: Create AWS Account Groups
Create two groups for the AWS account: Developers and QA.  
For Developers, grant the administrative policy. For QA, grant full EC2 access.

1. Go to [AWS](https://aws.amazon.com).
2. Log in to your account as a root user.
3. Navigate to IAM under **AWS services > Security, Identity & Compliance**.
4. Under IAM resources, navigate to **User groups**.
5. Click **Create group**.
6. Under **Create user group**, enter the group name `Developers`.
7. In the search bar, type `AdministratorAccess` and press enter. Then, select the policy and click **Create group**.
8. Create another group called `QA` and give it the `AmazonEC2FullAccess` policy.

## Lab Task 2: Create AWS Account Users
Create two users for the AWS account: Erin and Aaren. Add Erin to Developers and add Aaren to QA.

1. Navigate to **Users** under **Access management**. Then, click **Add users**.
2. The first user’s name should be `Erin`. Select **AWS Management Console access**. Leave the default settings for the other options and click **Next: Permissions**.
   
   > **Note:** You can add multiple users under the same policies.

3. In the **Add user to group** area, select `Developers` and click **Next: Tags**.
4. Do not add information under **Add tags**. Click **Next: Review**, and then click **Create user** on the next page.

   > **Good to Know:** Tags are utilized to add information about the user and are helpful tools for automation.

5. Click **Download .csv** to obtain the user’s login and URL credentials. Then, click **Close** in the bottom right corner.
6. Log in as an IAM user with Erin. Use the link/credentials provided in the .csv file and access the login page via the console login link in the .csv file (spreadsheet). AWS will force you to change the password upon your initial login.
7. While logged in with the Erin user, create another user named `Aaren`. Add Aaren to the `QA` group and download the .csv file, following Steps 1–5 of Task 2 that you used for Erin.
8. Log in as Aaren and try to create a user with the details in the last .csv file you downloaded. Note that this cannot be done due to user restrictions.
