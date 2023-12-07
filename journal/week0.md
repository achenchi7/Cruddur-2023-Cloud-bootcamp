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
I created a budget in AWS through the CLI using the following [block of code](aws/json/budget.json) and created a [budget notification with subscribers](main/aws/budget-notification-with-subscribers.json)
