


# Introduction

The backbone of all [operational stacks](/Project-Overview/Agile-Patterns-and-DevOPS-processes/The-Operational-Stacks.md) (DevOPS,MLOPS, DevSecOPS etc..) is the **_Continuous Integration/Continuous Deployment_**(**_CI/CD_**) pipelines that form the integration layer between development and released final product that can be consumed by the customer or other systems.

Looking at the diagram below we can quickly identify a few areas that signify important stages in the DevOPS process,
in this document we are going to review some of the most prominent processes below.
![A Common CI/CD Pattern](/.attachments/image-7a4e6127-938b-4db7-9663-e8c975f63fdc.png)



# Triggers and Gates

In order for us to initiate a process in our CI/CD Pipeline flow we need triggers and gates, **_triggers_** initiate and **_gates_** act as semaphores that provide appropriate control in the flow of the process.

## Triggers

There can be many triggers in a pipeline, one of the most common triggers are the **_build trigger_** in the CI Pipeline,
This is normally based on a merge action from a pull request and possibly a path filter, in other words PR to merge main branch into the **_release branch_** where a specific folder is affected.

## Gates
In order for us to control processes that has potential business risk associated with them such as a deployment action etc, we require signoff and acceptance of responsibility, in our pipelines it is recommended to automate as much as possible, but ultimately most actions that carry business risk should have a manual review gate, for instance before we start our environment promotion of code into staging and production, we should have a review gate where someone ultimately accepts responsibility for the release cycle and the features being released to the customer.

# The CI Pipeline

**_The need for continuous integration(CI) between development and production can be described by the following illustration:_**

_When embarking on a change, a developer takes a copy of the current code base on which to work. As other developers submit changed code to the source code repository, this copy gradually ceases to reflect the repository code. Not only can the existing code base change, but new code can be added as well as new libraries, and other resources that create dependencies, and potential conflicts._

_The longer development continues on a branch without merging back to the mainline, the greater the risk of multiple integration conflicts and failures when the developer branch is eventually merged back. When developers submit code to the repository, they must first update their code to reflect the changes in the repository since they took their copy. 
The more changes the repository contains, the more work developers must do before submitting their own changes._

_Eventually, the repository may become so different from the developers' baselines that they enter what is sometimes referred to as "merge hell", or "integration hell", where the time it takes to integrate exceeds the time it took to make their original changes._

Whilst the above illustration highlights a dystopian fate for the developer, the **CI pipeline will not alone save the developer** but this needs to be seen as the automation piece that fits into a well thought out [branch strategy](/Project-Overview/Agile-Patterns-and-DevOPS-processes/Branch-Strategy.md) and [agile development practice](/Project-Overview/An-Introduction-to-agile-development-practices/What-is-Agile-Development-practices).



## Build

The need to compile code into collections of deployable build artefacts is the most crucial and fundamental part of the CI Pipeline, this sets out the foundation that we base our deployments to our test, staging and production environments.
We also use the build pipeline to execute some of the fundamental unit tests such as static application security testing(SAST), language compliance, environment setup compliance and more.


## Testing

Unlike the fundamental tests that are completed in the Build process testing in the test stage is functional testing with agreed test outcomes and serves as a gate for the code to be surfaced for final acceptance testing of the product by a customer representative.

# The CD Pipeline

Continuous deployment(CD) pipeline is a software engineering approach in which software functionalities are delivered frequently through automated deployments. 
CD contrasts with continuous delivery, a similar approach in which software functionalities are also frequently delivered and deemed to be potentially capable of being deployed but are actually not deployed, _continuous delivery is what happens after the Build process publishes the build artefact_.

## Review

The 1st step in the CD pipeline is a UAT outcome review, this is when the business lead reviews the test activities and agrees that the deliverables are acceptable and meets the customers' expectations regarding form and functionality. 

## Stage Deployment

Deploying into a Stage environment is generally meant to provide a pre-production environment where production grade stress tests can be performed and full production cycles can occur, this is an accepted standard environment, but it is not required.


## Production Release

The final stage in the CD pipeline is the release into production, dep

[Back](#javascript:history.back())