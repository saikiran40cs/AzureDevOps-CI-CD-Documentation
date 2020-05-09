# Create Release Pipeline for ADO

An **artifact** is a deployable component of your application. It is typically produced through a Continuous Integration or a build pipeline. Azure Pipelines releases can deploy artifacts that are produced by a wide range of artifact sources such as Azure Pipelines build, Jenkins, or Team City.

You define the **release pipeline** using stages, and restrict deployments into or out of a stage using [approvals](https://docs.microsoft.com/en-us/azure/devops/pipelines/release/approvals/?view=azure-devops). You define the automation in each stage using jobs and tasks. You use [variables](https://docs.microsoft.com/en-us/azure/devops/pipelines/release/variables?view=azure-devops) to generalize your automation and [triggers](https://docs.microsoft.com/en-us/azure/devops/pipelines/release/triggers?view=azure-devops) to control when the deployments should be kicked off automatically.

An example of a release pipeline that can be modeled through a release pipeline in shown below:

![Artifacts in a pipeline and release](https://docs.microsoft.com/en-us/azure/devops/pipelines/release/media/definition-01.png?view=azure-devops)

In this example, a release of a website is created by collecting specific versions of two builds \(artifacts\), each from a different build pipeline. The release is first deployed to a Dev stage and then forked to two QA stages in parallel. If the deployment succeeds in both the QA stages, the release is deployed to Prod ring 1 and then to Prod ring 2. Each production ring represents multiple instances of the same website deployed at various locations around the globe.

