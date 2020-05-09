---
description: Pipeline creation
---

# Create Pipeline for Azure DevOps

This is a step-by-step guide to using Azure Pipelines to build a GitHub repository.

### Prerequisites <a id="prerequisites"></a>

* A GitHub account, where you can create a repository. If you don't have one, you can [create one for free](https://github.com/).
* An Azure DevOps organization. If you don't have one, you can [create one for free](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/pipelines-sign-up?view=azure-devops). \(An Azure DevOps organization is different from your GitHub organization. Give them the same name if you want alignment between them.\)

  If your team already has one, then make sure you're an administrator of the Azure DevOps project that you want to use.

 Note

If you want create a new pipeline by copying another pipeline, see [Clone a pipeline](https://docs.microsoft.com/en-us/azure/devops/pipelines/create-first-pipeline?view=azure-devops&tabs=java%2Cyaml%2Cbrowser%2Ctfs-2018-2#clone-a-pipeline).

### Create your first pipeline <a id="create-your-first-pipeline-1"></a>

* [Java](https://docs.microsoft.com/en-us/azure/devops/pipelines/create-first-pipeline?view=azure-devops&tabs=java%2Cyaml%2Cbrowser%2Ctfs-2018-2#tabpanel_CeZOj-G++Q_java)
* [.NET](https://docs.microsoft.com/en-us/azure/devops/pipelines/create-first-pipeline?view=azure-devops&tabs=java%2Cyaml%2Cbrowser%2Ctfs-2018-2#tabpanel_CeZOj-G++Q_net)
* [Python](https://docs.microsoft.com/en-us/azure/devops/pipelines/create-first-pipeline?view=azure-devops&tabs=java%2Cyaml%2Cbrowser%2Ctfs-2018-2#tabpanel_CeZOj-G++Q_python)
* [JavaScript](https://docs.microsoft.com/en-us/azure/devops/pipelines/create-first-pipeline?view=azure-devops&tabs=java%2Cyaml%2Cbrowser%2Ctfs-2018-2#tabpanel_CeZOj-G++Q_javascript)

#### Get the Java sample code <a id="get-the-java-sample-code"></a>

To get started, fork the following repository into your GitHub account.Copy

```text
https://github.com/MicrosoftDocs/pipelines-java
```

#### Create your first Java pipeline <a id="create-your-first-java-pipeline"></a>

1. Sign in to your Azure DevOps organization and navigate to your project.
2. In your project, navigate to the **Pipelines** page. Then choose the action to create a new pipeline.
3. Walk through the steps of the wizard by first selecting **GitHub** as the location of your source code.
4. You might be redirected to GitHub to sign in. If so, enter your GitHub credentials.
5. When the list of repositories appears, select your desired sample app repository.
6. Azure Pipelines will analyze your repository and recommend a Maven pipeline template. Select **Save and run**, then select **Commit directly to the master branch**, and then choose **Save and run** again.
7. A new run is started. Wait for the run to finish.

Learn more about [working with Java](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/java?view=azure-devops) in your pipeline.

