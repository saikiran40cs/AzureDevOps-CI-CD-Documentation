# Updating Code with fetch and pull

Distributed version control systems such as Azure Repos enable teams of developers to work on code and commit changes at the same time. Therefore, there are times when you cannot be sure you have the latest version of the code. WHen this is the case, you will need to execute some Git commands to ensure you have the latest version in your local repository:

* `fetch` - downloads the changes from your remote repo, but does not apply them to your code. This allows you to take a look at the changes before applying them.
* `merge` - applies the changes taken from a fetch to a branch on your local repository. Once you have looked at the fetched changes and decided they are suitable to add to your code, you choose to `merge`.
* `pull` - combines the above, does a `fetch` and then a `merge`.

To simulate another developer making a change and pushing it to the Azure Repo, switch back to the Azure DevOps portal, click **Files** under the **Repos** menu item on the left hand side, and click on the README.md filename to open the file in **Preview**:

![Azure DevOps Repos File Preview](https://csprodstorage001.blob.core.windows.net/blog/step4-fetchpull-preview.png)

If Azure DevOps knows how to display a filetype, such as Markdown, it will open in file preview, formatting the file appropriately. To edit the file click **Edit** top right:

![Azure DevOps Repos File Preview Edit](https://csprodstorage001.blob.core.windows.net/blog/step4-fetchpull-edit.png)

Edit the file and change the heading **Getting Started**, click **Commit** in the top right, you will now be prompted to enter a commit message:

![Azure DevOps Repos Commit Message](https://csprodstorage001.blob.core.windows.net/blog/step4-fetchpull-commitmessage.png)

Enter your commit message and click **Commit** at the bottom, in the background Azure DevOps is executing the same `git commit -m` command you used in an earlier step. The difference being that Azure DevOps is commiting the change to the Azure Repo and not locally. So if you switch back to VSCode and edit the README.md file, you will see that the heading still says Getting Started.

The local repository and the Azure Repo are now out of synch, to have the change reflected in the local repository you _pull_ the changes to your local repository. This will execute a `git fetch` and a `git merge`:

![Azure DevOps Repos Commit Message](https://csprodstorage001.blob.core.windows.net/blog/step4-fetchpull-pull.png)

The change made in Azure DevOps has now been pulled down to the local repository, if you switch back to VSCode, the change to the header line is now visible.

