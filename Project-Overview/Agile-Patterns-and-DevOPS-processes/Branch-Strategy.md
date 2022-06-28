# Summary
This documents a few popular branch strategies and their appropriate implementation scenarios,
in the table below you can find a quick breakdown of these and how they might suit your operation:


| **Strategy** | **Strength** | **Weakness** | **Notes** |
|--|--|--|--|
| **Single/No Branch Strategy** | Simple to manage where there is a single developer per tech stack/target system. | Can create complex merge conflicts that can be extremely hard to resolve (depending on technology stack), can make it hard to roll back defective released features. | This strategy is primarily designed for small, isolated teams with no to little collaboration. |
| **Feature Branch Strategy** | Creates granular control of individual features where small to large teams with cross stack responsibility can easily manage the release and rollback of individual features. | Does require well developed agile processes and procedures. | This strategy aligns most with professional agile teams and is the most recommended process. |
| **Sprint Branch Strategy** | Fairly simple to implement and fairly simple to manage, it is a traditional DevOPS strategy that generally aligns with software development teams. | Can cause merge conflicts during the pull requests, this is largely dependent on the target technology or stack. | When working in non-compiled environments where build the build manifests are managed in the compiler and not in the IDE this makes this approach the ideal choice. |


Regardless of what strategy we use, we must always work with the concept of a **_release branch_**, this branch creates the isolation layer between working code and build and release pipelines.

Below is a set of examples of how this would look in a feature branch scenario:

![image.png](/.attachments/image-6432f7ad-716e-47ef-9e46-f7834d8c0686.png)



# Examples by Target stack

For a step by step example on how to implement this for Azure Data Factory and Synapse Analytics Workspaces [**click here.**](/Project-Overview/Agile-Patterns-and-DevOPS-processes/Branch-Strategy/Azure-Data-Factory-and-Synapse-Analytics-Workspaces.md)
and for Azure SQL DB in Visual Studio SSDT **click here**. 





[Back](#javascript:history.back())


