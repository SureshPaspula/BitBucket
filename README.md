# BitBucket pull Requests

#### Introduction
* Pull requests allow developers to effectively collaborate using code. Instead of having to push a change to the main version of a project, a developer can submit a pull request. This method allows them to facilitate feedback on their code.
* Because pull requests don’t involve changing the main version of a codebase, they are also a great tool for code review. If there are any bugs in your code or any ways in which your code could be improved, they could be addressed directly within the pull request.
* There’s no need to worry whether bugs have been introduced into the main codebase; a pull request is stored in isolation from the main version of a project. 
* The code in a pull request may be a work in progress. This is because it will not affect the main version of a code until a git merge operation is run or the pull request is moved into the main version of a project by the project maintainer.

#### Create a local repo and create a branch
*  We are going to create a copy of our repository on our local machine. 
* You can create a copy of a repository using the git clone command line operation:
  ```
  git clone repositoryURL
  cd repository_name
  ```
* These commands create a local working copy of our code to which we can make changes and move our terminal session into the project folder. To learn more about the git clone command
* The next step is to create a branch on which we can make our changes. A branch is like another version of a repository within a repository. The default branch for a repository is called master, and is where the main version of a codebase is usually stored. Developers use branches to keep track of different versions of their code.
* Suppose we want to modify the README.md file in our code. To do so, we’re going to create a branch called “update-docs” which will contain our updated code. We can do so using this code:
  ```
  git checkout -b update-docs
  ```
* Make your branch name descriptive. For example, naming it "feature/XYZ" if it's a new feature and is about XYZ is easy to let anyone know what the branch is for.
* The first command creates a new branch called “update-docs” and then changes our Git session to view the code on the update-docs branch.

#### Make changes
* For this example, we are going to change our README.md to contain the following:
  ```
  * Test - Pull Request
  * An example change of how pull request works
  ```
* When we save this file, our changes will be made on our local machine. But, these changes will not yet be saved to our repository. This is because Git is a distributed version control system and changes are only made to a repository when you commit them.
* Before we commit our changes, we need to use “git add” to add those changes to a Git commit:
  ```
  git add .
  ```
* You can commit a change to a repository using the git commit command. When you use this command, you’ll need to provide a short message which describes the changes you have made. 
* In this example, we’re going to add the message “docs: Added created by to README.md”, which briefly tells other developers what changes we have made.
  ```
  git commit -m "docs: Added created by to README.md"
  ```
* At the moment, our commit is only stored on our local copy of the repository. That’s because we haven’t pushed our code to our main repository. “Pushing” is when you upload the changes you have made locally to the main version of a repository.
* You can push your code using this command:
  ```
  git push --set-upstream origin update-docs
  ```
* In the repository in bitbucket, go to the 'Pull requests' tab, and click "Create pull request". And your PR is created. 
* In this form we can specify the name of our pull request (which is automatically set as the commit message of your most recent change) and the description for our pull request. Then you can choose reviewers who you want this code to be reviwed 






   