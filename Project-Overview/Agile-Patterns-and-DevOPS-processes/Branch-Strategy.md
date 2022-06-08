[[_TOC_]]


# **Azure Data Factory**


When Working with the CI/CD integrated Azure Datafactory it is important to understand that all User stories that are being worked on require a feature branch per story. 

This means that each User story is worked on in isolation and this will minimize the possibility of merge conflicts.

The feature branching pattern is as demonstrated below:




##Process Diagram
::: mermaid
 graph LR;
 A[Sprint Planning] --1 Sprint Branch --> B[Work Start];
B --2 Feature A Branch --> C[Feature A work done];
B --2 Feature B Branch --> D[Feature B work done];
C --3 PR to Sprint Branch--> E[Merge to Sprint];
D --3 PR to Sprint Branch--> E;
E --4 PR to Main --> F[Sprint Retro];
F --5 PR Approved--> G[Publish to Main];
G --6 PR to ADF Release --> H[Features in UAT];
:::



##Process Details:
1. At start of every sprint the team lead created a sprint branch based on _**release branch**_ using the following naming convention:
   - **_{SprintName}-{YYYYMMDD}_**
![image.png](/.attachments/image-7f338e6b-110b-4d3d-9046-1ec01cbb7fda.png)
2. Before a developer starts work on a user story they create a branch in data factory based on the sprint branch created in step 1using the following naming convention:
   - **_{SprintName}-{YYYYMMDD}-{Story ID}_**
![image.png](/.attachments/image-c7e2c2a9-9d19-470d-b404-546c75481c63.png)
3. Once the developer has built and tested their pipelines in the use story the raises a _**pull request (PR)**_ to merge into the Feature branch into main 
![image.png](/.attachments/image-90f879ed-8833-4c66-bc2e-6d7b11558809.png)
4. During the sprint retro the PR is reviewed and 
5. as part of the retro the **_PR is approved_**
6. The CI/**CD** release pipeline deploys to the UAT Factory


