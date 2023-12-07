# Week 0 — Billing and Architecture
## Install AWS CLI
I used the following commands to install AWS CLI on Linux using Gitpod
```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install

```
## Configure AWS CLI
The AWS CLI is an open-source tool that allows you to interact with AWS services through the command line shell.
I configured the AWS CLI to store my account credentials through the following steps:
- set your AWS credentials using the command ```aws configure```
- Input your credentials: AWS secret access key, Access key ID, Default region name, Default output name.
- The command ```env | grep aws``` shows you the credential you have set
- To commit the credentials to memory run the command ```gp env AWS_ACCOUNT_ID```



## Create a budget and notification
I created a budget in AWS through the CLI using the following [block of code](aws/json/budget.json) and created a [budget notification with subscribers](budget-notification-with-subscribers.json) **look into the links**



## Logical AWS architecture
I created a logical AWS architecture for the **Cruddur project**, an ephemeral micro blogging platform.
[Logical AWS architecture](https://lucid.app/lucidchart/54797646-a30f-46fe-9ceb-158c13ae2af2/edit?viewport_loc=-3497%2C-843%2C8635%2C4250%2C0_0&invitationId=inv_af839e59-cc78-4bcb-838c-bd6727e1cded)

### Why the services?
- #### Amazon Route 53

