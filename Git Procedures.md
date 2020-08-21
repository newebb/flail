This guide summarizes common procedures for students using the StMU-UAV GitHub repository. For an in-depth tutorial on installing Git and Git commands, see  [Git Tutorials and Training | Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials).

The master branch stores the current version of SMUC which has been finalized and tested. **Do NOT commit directly to the master branch.** Instead, commit to a branch for your project. You may choose to create new branches from your project branch for testing code. 

# Download repository:

**Using Terminal or Command Prompt:**

The following command will make a local clone of the StMU-UAV repository:

```
git clone https://github.com/STMU-DroneLab/StMU-UAV.git
```

---

**Using the website:** 

In the **<> Code** tab, Download the ZIP package or clone with HTTPS to an IDE with git plugin: 

![](https://raw.githubusercontent.com/newebb/flail/master/Download.png)

# Create and Check Out Branches:

The branches stored on GitHub are remote branches. The checkout command makes a local working copy of the branch. Windows/Mac users do not have to check out branches if using GitHub Desktop.

**Using Terminal or Command Prompt:**

Navigate to the cloned repository. 

The following command will create a new branch and check out a new branch:

```
git checkout -b <New Branch Name>
```

The following command will create a remote branch with the same name as what you created, as well as configure the tracking reference.

```
git push --set-upstream origin <New Branch Name>
```

To checkout an existing remote branch,  the following command will checkout that branch and store it in a new local branch with the same name:

```
git checkout --track origin/<Branch Name>
```

---

**Using the website:**

In the **<> Code** tab, Click the **Switch branches or tags** drop-down menu and select the master (default) branch.

![](https://raw.githubusercontent.com/newebb/flail/master/Switch%20branches.png)

Click the drop-down menu again and type your new branch name.

![](https://raw.githubusercontent.com/newebb/flail/master/Branch%20name.png)

Select **Create branch: <Branch name> from '<Branch Created From>'**

Follow the procedure to checkout the project branch for your specific IDE with git plugin. 

# Making and Pushing Commits:

Commits track changes of files in the GitHub repository. Commits will not be sent to the remote repository until they are pushed. Make commits to your local branch, and then push the commits to the remote (checked out) branch.  

The commit message consists of a summary and description. The summary shows on the timeline and should be a concise summary of changes made by your commit. If the list of changes does not fit on one line, continue into the description. 

**Using Terminal or Command Prompt:**

The commit command has several options. The following command commits all the changes made in your local working directory. 

```
git commit -a
```

You will then be prompted for a commit message. The first line contains the summary. Leave the second line blank. The third line on contains the description. 

The push command pushes any commits made:

```
git push origin <branch name>
```

---

**Using IDE with git plugin** 

Select the files changed (unstaged changes) and add a commit message. Select commit if adding another commit. Select "Commit and push" if ready to send to the remote repository.

# Create a Pull Request:

Create a pull request once you are finished writing and debugging your code.  

To create a pull request directly through GitHub, go to the **Pull requests** tab and click **New pull request**.

![](https://raw.githubusercontent.com/newebb/flail/master/New%20pull%20request.PNG)

Next select the base reference (branch being merged to) and the head reference (branch you committed to). Fix conflicts if the branches cannot be merged automatically. Select **Create new pull request**.

![](https://raw.githubusercontent.com/newebb/flail/master/Comparing%20changes.PNG)

Your branch will be merged once changes are reviewed. 
