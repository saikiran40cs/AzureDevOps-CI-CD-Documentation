---
description: How to create a new repository
---

# Create Repository

A repository is a place to store version controlled code, enabling one or more developers to collaborate on the code, keeping a history of all changes. This is known as source control. You'll be adding a project which will automatically create a repository, this will enable you to add code and make changes to that code in further steps, simulating how an individual or team works with source control.

For this step you want to be working with a repository so choose **Repos**.

![View empty Repo](https://csprodstorage001.blob.core.windows.net/blog/step1-azuredevops-emptyrepo.png)

This is a view of an empty repository, to work with this repository locally, either from the command line or from a client, you will need to generate credentials. On this page you can see a button marked **Generate Git Credentials**, this will allow you to set a username and simple password to work with the repository. However it is not recommended, as these credentials have full access to the repository, along with other services and do not expire. The Microsoft Docs article [Authentication overview](https://docs.microsoft.com/en-gb/azure/devops/repos/Git/auth-overview?view=azure-devops) for Azure DevOps recommends to use a Personal Access token, where scope of access and an expiration date can be set.

