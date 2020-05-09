# Pushing an existing repository from the command line

You've explored working with a repository created with Azure DevOps, by cloning that repository locally, pushing to, and pulling changes from the Azure Repo. What happens if you have already got a local repository and need to push that repository to a new Azure DevOps project? To simulate this you need to _intialise_ a new git repository locally, you uwill then add a README to this repository and push it to a new Azure DevOps project.

Initialising a repository creates an empty repository using the same method utilised by Azure DevOps in Step 1. Both of these processes both use the `git init` command. When executing the command locally, it must be executed within folder that does not already contain a git repository, however, the folder does not have to be empty:

![Local repository initialisation](https://csprodstorage001.blob.core.windows.net/blog/step5-localinit-gitinit.png)

The process here is to make a new empty folder using `mkdir` on the command line, `cd` into that folder and then execute `git init`. The section highlighted above shows the Git repository being initialised and then `dir /a /b` \(`ls -al` on a Mac\) to display that the repository is empty, apart from the newly created .git folder.

Next you need to add a file to simulate code being present in the local repository. Execute `code .` on the command line to launch VSCode within the repository and then create a README.md file for the repository:

![Local repository initialisation](https://csprodstorage001.blob.core.windows.net/blog/step5-localinit-createreadme.png)

Enter some text within the file and save. Switch back to the command line and execute `git status` to verify that Git has picked up the change on the file system. Now execute `git add .` to stage all changes ready for commit, then commit the change using `git commit -m` and add an appropriate message:

![Local repository add and commit README](https://csprodstorage001.blob.core.windows.net/blog/step5-localinit-commitreadme.png)

You now need to create a new project within Azure DevOps, so switch to the Azure DevOps portal and click **Azure DevOps** top right to return to your Azure DevOps organisation, click **New project** in the top right hand corner, this opens the add project page:

![Local repository create Azure DevOps project](https://csprodstorage001.blob.core.windows.net/blog/step5-localinit-createproject.png)

The create project page displayed is slightly different than the one displayed for a new Azure DevOps organisation. You will need to enter the **Project name**, making it the same as the folder name of your local repository. If you scroll to the bottom of the page, you can also select **Version control** which always defaults to Git, but can be changed to Team Foundation Server. Click **Create** to create the new project. When the new project is created, click on **Repos** in the services menu on the left, you will see the same empty repo page as viewed in step 1. Scroll down to **Push an existing repository from command line**:

![Url for origin remote](https://csprodstorage001.blob.core.windows.net/blog/step5-localinit-pushurl.png)

Here you can see the URL for the _remote_ called origin. A remote repository in Git is a version of the project hosted either on the internet or on a local network, in the case of this guide, within Azure DevOps. Origin is just the default name for the URL, it's shorthand name. If you execute `git remote` from inside a repository, all remotes for the repository are listed:

![List repository remotes](https://csprodstorage001.blob.core.windows.net/blog/step5-localinit-listgitremotes.png)

You have a new locally intialised repository with no remotes, so none are listed at this stage. Switch back to Azure DevOps and copy the first part of the command for pushing an existing repository:

![Add remote called origin](https://csprodstorage001.blob.core.windows.net/blog/step5-localinit-addremoteorigin.png)

The remote has been added and re-issuing `git remote` lists origin as a remote. You now need to push your changes up to the origin, to do this execute `git push origin master`, this pushes all changes from the local master branch to the origin:

![Push local master to origin](https://csprodstorage001.blob.core.windows.net/blog/step5-localinit-gitpushoriginmaster.png)

Switch back to Azure DevOps portal, click **Repos** and then **Files** on the services menu for the localgitinitdemo project, the Repo now reflects the repository pushed up from local:

![Push local master to origin](https://csprodstorage001.blob.core.windows.net/blog/step5-localinit-changesinazurerepo.png)

