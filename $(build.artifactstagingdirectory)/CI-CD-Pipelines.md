[[_TOC_]]


# Introduction

The backbone of all [operational stacks](/Project-Overview/Agile-Patterns-and-DevOPS-processes/The-Operational-Stacks) (DevOPS,MLOPS, DevSecOPS etc..) is the **_Continuous Integration/Continuous Deployment_**(**_CI/CD_**) pipelines that form the integration layer between development and released final product that can be consumed by the customer or other systems.

Looking at the diagram below we can quickly identify a few areas that signify important stages in the DevOPS process,
in this document we are going to review some of the most prominent processes below.
![A Common CI/CD Pattern](/.attachments/image-7a4e6127-938b-4db7-9663-e8c975f63fdc.png)



#Triggers and Gates
In order for us to initiate a process in our CI/CD Pipeline flow we need triggers and gates, **_triggers_** initiate and **_gates_** act as semaphores that provide appropriate control in the flow of the process.
##Triggers
There can be many triggers in a pipeline, one of the most common triggers are the **_build trigger_** in the CI Pipeline
#The CI Pipeline
##Build
##Testing
#The CD Pipeline
##Review
##StageDeployment
##Production Release