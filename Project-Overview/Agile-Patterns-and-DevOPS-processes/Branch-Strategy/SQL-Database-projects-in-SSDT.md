# **SQL Database projects in SSDT (Visual Studio)**


When Working with SQL Server projects for analytics there are two best practices when working with deployable packages, they are:

- Branch Strategy.
- Feature Branch Strategy. 

The only **_real_** difference between the above two strategies are the amount of granularity that is available for rolling back individual development efforts and how many changes are managed in each pull request.

As with the Azure Data Factory CI/CD examples, the same pattern is true and valid but has however different tooling available, below is an example on how to perform a Feature branch strategy in Visual Studio SQL Server Data Tools.


The feature branching pattern is as demonstrated below:




## Process Diagram

![image.png](/.attachments/image-01043a8c-8fb6-453b-b73b-8f6125c3cecd.png)




## Process Details:

1. At start of every sprint the team lead created a sprint branch based on _**release branch**_ using the following naming convention:
    **_{SprintName}-{YYYYMMDD}_**
   - This is done in two steps, in SSDT click on the **_Branches_** hub in the Team Explorer window:

     ![image.png](/.attachments/image-90e4d4fc-8310-4ab3-ae46-ab3ba13ae38a.png)
   - Right Click the Release Branch Click _**New Local Branch From..**_
   - Provide the appropriate new branch name in the New Brach field,
   - Endure it is based on the Release branch.
   - Click **_Create Branch_**

     ![image.png](/.attachments/image-34932507-23ee-44e2-a231-2d55113bf7f2.png)

   - Now **_Right Click the new branch_** and click **_Push Branch_**

     ![image.png](/.attachments/image-79d56821-fb49-43a8-8c96-fc07e64883d7.png)
     
     At this point you should be met with a Success message and **_the repo should be ready for the Sprint to begin_**.

     ![image.png](/.attachments/image-ddf35f47-02e7-4ec9-87d0-596c4e17da46.png)


2. Before a developer starts work on a user story they create a branch in data factory based on the sprint branch created in step 1using the following naming convention:
    **_{SprintName}-{YYYYMMDD}-{Story ID}_** by following the above steps from point 1 **_but instead of basing it on the release branch rather base it on the Iteration branch_**.
   
    ![image.png](/.attachments/image-894a7504-b062-478f-aef2-3a6ebf2cce90.png)



3. Once the developer has built and tested their code in the user story repo, it is time to create a _**pull request (PR)**_ to merge into the Feature branch into Sprint Branch.
   This is achived by right clicking the user story/feature branch and click Create Pull Request

   ![image.png](/.attachments/image-7e58c9ac-0edf-465f-bc35-7600bfe74a8b.png)
   
   This opens the pull request dialogue in Azure DevOPS.

   ![image.png](/.attachments/image-991c1480-0a57-4d40-979d-c1e90caea436.png)


4. During the sprint retro the PR is reviewed and 
5. as part of the retro the **_PR is approved_**
6. The CI/**CD** release pipeline deploys to the UAT environment.


<a href = "javascript:history.back()">Back to previous page</a>