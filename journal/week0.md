# Week 0 — Billing and Architecture

The first week of the bootcamp was dedicated to an introduction to the business scenerio which is the use-case problem to be solved and some other tools needed to be able to achieve some different tasks and make our work easier in the bootcamp.  

We also talked alot about AWS billing and cost management services because it's as important as anything else, as we would want to make sure I don't go above the aws free tier limits in my aws account or whatever I have as a budget when working on a project. So we talked about AWS services that can help us track of our expenses like;

1. AWS budgets
2. Billing alerts

## Completed Assignments

### 1. Setting Up AWS Account and Security Credntials

Since I've been using AWS for about a year plus I already had my account setup and I had programmatic access credentials as well using Access keys and secret access keys. So I did not need to create new ones.

### 2. Recreating Conceptual Diagram in Lucid Charts or on a Napkin

I recreated the conceptual diagram and also the logical diagram of the application using Lucid charts, previously I used draw.io for architectual diagrams, hence this was my first time using lucid charts and I think they're both similar. Here is the conceptual  diagram.
![Cruddur Conceptual Diagram!](/_docs/assets/Cruddur-Conceptual-Diagram.jpg)  

And here is the logical architectural diagram.
![Cruddur Logical Diagram!](/_docs/assets/Cruddur-Logical%20Diagram.png)

## 3. Create a Budget/Billing Alarm

I already had a budget set up for for my personal projects on AWS.
![Budget!](/_docs/assets/Budgets.png).  

Here's my Billing alarm  
![Alarm!](/_docs/assets/Billing%20Alarm.png)

I practiced creating a budget using the AWS CLI with a [Budget.json file](https://github.com/Aa-kk/aws-bootcamp-cruddur-2023/blob/main/aws/json/budget.json) to create the budget and [budget-notifications-with-subscribers.json file](https://github.com/Aa-kk/aws-bootcamp-cruddur-2023/blob/main/aws/json/budget.json) to set up the notifcation and subscribers.  

using this command:  
`aws budgets create-budget \`  
    `--account-id AccountID \`  
    `--budget file://aws/json/budget.json \`  
    `--notifications-with-subscribers file://aws/json/budget-notifications-with-subscribers.json`

## Setting Up Gitpod and configuring the AWS CLI

First time I got to use gitpod and I think it's a cool tool (Cloud based DE) for developers.  After setting up a gitpod account and installing the plugin in my browser I installed the AWS CLI manually and also configured Gitpod to always have the AWS CLI installed into every workpace using the by assiging the process as a task in the [.gitpod.yml](https://github.com/Aa-kk/aws-bootcamp-cruddur-2023/blob/main/.gitpod.yml)  

Adding my aws credentials to gitpod was pretty easy using  
`gp env AWS_ACCESS_KEY_ID=""`  
`gp env AWS_SECRET_ACCESS_KEY=""`  
`gp env AWS_DEFAULT_REGION=eu-central-1`

The above commands tells gitpod to remember these enviromental variables so you don't have to set them everytime you open a workspace.
