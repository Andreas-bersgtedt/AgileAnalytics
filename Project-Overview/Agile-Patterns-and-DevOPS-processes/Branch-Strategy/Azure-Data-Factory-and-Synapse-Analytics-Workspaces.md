# **Azure Data Factory / Synapse Analytics Workspaces**


When Working with the CI/CD integrated Azure Data Factory / Synapse Analytics Workspaces it is important to understand that all User stories that are being worked on require a feature branch per story. 

This means that each User story is worked on in isolation and this will minimize the possibility of merge conflicts.

The feature branching pattern is as demonstrated below:




## Process Diagram

![image.png](/.attachments/image-01043a8c-8fb6-453b-b73b-8f6125c3cecd.png)




## Process Details:

1. At start of every sprint the team lead created a sprint branch based on _**release branch**_ using the following naming convention:
    **_{SprintName}-{YYYYMMDD}_**

![image.png](/.attachments/image-7f338e6b-110b-4d3d-9046-1ec01cbb7fda.png)

2. Before a developer starts work on a user story they create a branch in data factory based on the sprint branch created in step 1using the following naming convention:
    **_{SprintName}-{YYYYMMDD}-{Story ID}_**

![image.png](/.attachments/image-c7e2c2a9-9d19-470d-b404-546c75481c63.png)

3. Once the developer has built and tested their pipelines in the use story the raises a _**pull request (PR)**_ to merge into the Feature branch into Sprint Branch.

![image.png](/.attachments/image-90f879ed-8833-4c66-bc2e-6d7b11558809.png)

4. During the sprint retro the PR is reviewed and 
5. as part of the retro the **_PR is approved_**
6. The CI/**CD** release pipeline deploys to the UAT Factory
