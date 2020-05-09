---
description: Pipeline creation
---

# Create Pipeline for ADO

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

#### Get the .NET Core sample code <a id="get-the-net-core-sample-code"></a>

To get started, fork the following repository into your GitHub account.Copy

```text
https://github.com/MicrosoftDocs/pipelines-dotnet-core
```

#### Create your first .NET Core pipeline <a id="create-your-first-net-core-pipeline"></a>

1. Sign in to your Azure DevOps organization and navigate to your project.
2. Go to **Pipelines**, and then select **New Pipeline**.
3. Walk through the steps of the wizard by first selecting **GitHub** as the location of your source code.

   ![Select GitHub](https://docs.microsoft.com/en-us/azure/devops/pipelines/media/get-started-yaml/new-pipeline.png?view=azure-devops)

    Note

   If this is not what you see, then [make sure the Multi-stage pipelines experience is turned on](https://docs.microsoft.com/en-us/azure/devops/project/navigation/preview-features?view=azure-devops).

4. You might be redirected to GitHub to sign in. If so, enter your GitHub credentials.
5. When the list of repositories appears, select your repository.
6. You might be redirected to GitHub to install the Azure Pipelines app. If so, select **Approve and install**.

> When the **Configure** tab appears, select **ASP.NET Core**.

1. When your new pipeline appears, take a look at the YAML to see what it does. When you're ready, select **Save and run**.
2. You're prompted to commit a new _azure-pipelines.yml_ file to your repository. After you're happy with the message, select **Save and run** again.

   If you want to watch your pipeline in action, select the build job.

   > You just created and ran a pipeline that we automatically created for you, because your code appeared to be a good match for the [ASP.NET Core](https://github.com/Microsoft/azure-pipelines-yaml/blob/master/templates/asp.net-core.yml) template.

   You now have a working YAML pipeline \(`azure-pipelines.yml`\) in your repository that's ready for you to customize!

3. When you're ready to make changes to your pipeline, select it in the **Pipelines** page, and then **Edit** the `azure-pipelines.yml` file.

Learn more about [working with .NET Core](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/dotnet-core?view=azure-devops) in your pipeline.

