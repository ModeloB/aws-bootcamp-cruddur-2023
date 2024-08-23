# Week 0 — Billing and Architecture
I created a couple budgets as recommmended. One is for trackiung my credit spending and the other is the standard 'zero spend' budget
![Budgets](https://github.com/user-attachments/assets/9b9b2940-393b-4f7b-9e34-d97a93d2e852)

Getting the AWS CLI Working
We'll be using the AWS CLI often in this bootcamp, so we'll proceed to installing this account.

Install AWS CLI
We are going to install the AWS CLI when our Gitpod enviroment lanuches.
We are are going to set AWS CLI to use partial autoprompt mode to make it easier to debug CLI commands.
The bash commands we are using are the same as the [AWS CLI Install Instructions]https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
Update our .gitpod.yml to include the following task.

tasks:
  - name: aws-cli
    env:
      AWS_CLI_AUTO_PROMPT: on-partial
    init: |
      cd /workspace
      curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
      unzip awscliv2.zip
      sudo ./aws/install
      cd $THEIA_WORKSPACE_ROOT
We'll also run these commands indivually to perform the install manually
