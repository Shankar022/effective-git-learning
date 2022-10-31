## 1.  What is VCS
***
**Version control** is a system that records all changes and modifications to files for tracking purposes. Developers also use the term source control or source code management. The primary goal of any version control system is to keep track of changes. It achieves this by allowing developers access to the entire change history with the ability to revert or roll back to a previous state or point in time.


## 2. What Are The Benefits Of Version Control ( [Reference](https://reqtest.com/requirements-blog/what-are-benefits-of-version-control/) )
***
1. Traceability
2. Document History
3. Branching And Merging
4. Identity
5. Reduction Of Duplication And Errors
6. Management Overview
7. Open Channels Of Communication
8. Adherence To Compliance
9. Efficiency


## 3. Centralized vs Distributed Version Control Systems
***
1. **Centralized Version Control**

     - A centralized version control system works on a client-server model. There is a single, (centralized) master copy of the code base, and pieces of the code that are being worked on are typically locked, (or “checked out”) so that only one developer is allowed to work on that part of the code at any one time. Access to the code base and the locking is controlled by the server. When the developer checks their code back in, the lock is released so it’s available for others to check out.

    - Of course, an important part of any VCS is the ability to keep track of changes that are made to the code elements, and so when an element is checked in, a new version of that piece is created and logged. When everyone has finished working on their different pieces and it’s time to make a new release, a new version of the application is created, which usually just means logging the version numbers of all the individual parts that go together to make that version of the application.

    - Probably the best known examples of centralized VCS systems are CVS and Subversion, both of which are open source, although there have been many commercial examples (including IBM’s Rational ClearCase).


2. **Distributed Version Control**

    - More recently, there’s been a trend (or some might call it a revolution) toward distributed version control systems. These systems work on a peer-to-peer model: the code base is distributed amongst the individual developers’ computers. In fact, the entire history of the code is mirrored on each system. 

    - There is still a master copy of the code base, but it’s kept on a client machine rather than a server. There is no locking of parts of the code; developers make changes in their local copy and then, once they’re ready to integrate their changes into the master copy, they issue a request to the owner of the master copy to merge their changes into the master copy.

    - With a DVCS, the emphasis switches from versions to changes, and so a new version of the code is simply a combination of a number of different sets of changes. That’s quite a fundamental change in the way many developers work, which is why DVCS’s are sometimes considered harder to understand than centralized systems.

    - The best known examples of distributed VCS’s are Git and Mercurial, both of which are open source.


3. **Pros and Cons**

    - The key difference between centralized and distributed VCS’s, in my opinion, revolves around the fact that there is no locking of elements in a distributed system. So every new set of changes that a developer makes is essentially like a new branch of the code, that needs to be merged back into the master repository. In the distributed model, it’s possible for two developers to be working on the same source file at the same time. 

    - That one fundamental difference means that:

        1. Performance of distributed systems is better, because there is no waiting for locks to happen across potentially slow network connections. Also, the complete code base is already on your local system.

        2. Branching and merging is much easier to achieve in a distributed system, largely because it’s built in to the way the system works.

        3. With a distributed system, you don’t need to be connected to the network all the time.

    - For these reasons, many people have become DVCS fans and believe that Git and Mercurial are the answer to any VCS question. However, centralized systems like Subversion do have some benefits too:

        1. Centralized systems are typically easier to understand.

        2. Access control is easier, since everything is controlled from one place (the server).

        3. Unless you want to, you don’t have to merge different versions of the same code, which can be tricky.


***
## 4. Version control in professional software development
**Version Control** plays a crucial part in software development. As a developer, you’ll work with other developers on projects to deliver software to customers. Depending on the role, you could be working with a small team of 2 or 3 developers in a single project or a large team spanning multiple projects. In either scenario, Version Control will be a crucial tool to help your team succeed.

However, Version Control must be complemented by other tools and procedures to ensure quality and efficiency throughout the software development process. In this lesson, we’ll explore some of the common tools and strategies developers use in conjunction with Version Control.

1. **Workflow** 

    - Using Version Control without a proper workflow is like building a city without traffic lights; without appropriate management, everything will turn into chaos.

    - For example, let’s say you’re working on a big project and editing a file. Another developer also starts editing a file. Both of you submit the file to the VCS at the same time. Now there’s a conflict! How should the conflict be resolved? A good workflow will have a process for resolving conflicts.

    - Another example is when a new junior developer is joining your team. If the project code is used for a critical system, it is risky to allow them to submit code changes directly. To solve this, many developers use a peer review system where another developer must review code before it can be merged in.

    - Workflows are essential to ensure code is managed correctly and reduce mistakes from happening. Different projects will have different workflows. In this course, you’ll learn some common workflows using the Git Version Control System.

2. **Continuous Integration**

    - Continuous Integration, or CI, is used to automate the integration of code changes from multiple developers into a single main stream. Using a workflow whereby small changes are merged frequently, often many times per day, will reduce the number of merge conflicts.

    - This process is widespread in test-driven software development strategies. CI is often used to automatically compile the project and run tests on every code change to ensure that the build remains stable and prevent regressions in functionality.

3. **Continuous Delivery**

    - Continuous Delivery is an extension of Continuous Integration. Once the changes have been merged into the main stream, a Continuous Delivery system automatically packages the application and prepares it for deployment. This helps avoid human error when packaging the application.

4. **Continuous Deployment**

    - Continuous Deployment is an extension of Continuous Delivery. The goal of Continuous Deployment is to deploy and release software to customers frequently and safely. The strategy commonly involves automatically deploying to a test (also known as staging) environment first to validate the deployment package and software changes. Once validated, it can automatically deploy to the live (also known as production) environment for customers.

5. **Conclusion**

    - With these tools and procedures, it is possible to understand how software starts from a developer writing code to being deployed live for customers to use. Of course, there is much more to running a live software service, but that is a lesson for another day.


