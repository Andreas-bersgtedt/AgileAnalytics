# Introduction 
If the Agile Manifesto is the founding principles that define why we do what we do then DevOPS is the cornerstone of all integrated operational practices that define how we work.

The origins of the name DevOPS is generally agreed as being coined by Patrick Debois in 2009 during his presentation at his DevOpsDays conference, however it is important to understand that DevOPS has its origin from Grady Brooch's publication in 1991 called Object Oriented Analysis and Design With Applications, this publication as revised in 1994 sets the foundation for the Continuous Integration framework (CI) in the form of the Brooch method.

![image.png](/.attachments/image-1f3cb71f-7089-4597-8c4b-2304d9ec24b5.png)

# DevOPS

DevOPS is the operational framework that underpins how agile enterprise development teams standardise the way that they are able to operate, without the need to manage technical infrastructure or attend to infrastructure related activities.
For instance, a development team plan their activities, develop code that is then committed into source control and is pushed down a pre-defined build, test, release and deployment cycle, the team monitors performance telemetry and correlate this with feedback from the users and customers that is then fed back to the backlog and another planning cycle starts.

This is one of the most popular ways to work as an agile development team, if we look at the process described above the only interface points that truly concerned the team was:

- Plan
- Develop
- Commit

All other steps in the process were a [pre-determined pipeline](/Project-Overview/Agile-Patterns-and-DevOPS-processes/CI-CD-Pipelines.md) or performed by external parties.






# DevSecOPS

DevSecOps is the same as DevOPS but with the addition of **_Security_** testing gates, for instance, there are additional test gates and processes to execute during and before the [CI/CD pipeline](/Project-Overview/Agile-Patterns-and-DevOPS-processes/CI-CD-Pipelines.md) for example
Static Application Security Tests(SAST) where fundamental security policy compliance is tested.
In other words SAST processes enables an organisation to minimize policy violations regarding vulnerabilities such as stored credentials in code and introductions of vulnerabilities such as SQL injections etc.

It is widely agreed that the SAST processes are insufficient to comply with a DevSecOps framework and is generally supplemented with Dynamic Application Security Tests(DAST) or Interactive Application Security Tests(IAST) processes, these are designed tests that run as part of UAT or pre-production that simulates and monitors deployed code for vulnerabilities that are hard to detect during debug and development.

IAST runs from inside the code and looks for vulnerabilities in the binaries, whereas DAST processes are executed outside of the code to test external attack vectors for example: attack vectors against an API interface.  










[Back](#javascript:history.back())