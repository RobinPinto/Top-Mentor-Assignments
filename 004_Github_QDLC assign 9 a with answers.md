# Github_QDLC(L1)

1. What is GitHub?
2. How do you create a GitHub account?
3. What is a repository in GitHub?
4. How can you create a new repository on GitHub?
5. What is a README.md file, and why is it important in a GitHub repository?
6. How do you add files to a GitHub repository?
7. How can you commit changes to a repository in GitHub?
8. What is a pull request, and how do you create one?
9. What is a fork in GitHub?
10. How do you clone a repository to your local machine?
11. How do you push changes from your local machine to a GitHub repository?
12. What is a branch in GitHub, and why would you use it?
13. How can you merge a branch into the main/master branch?
14. What is the purpose of the "Issues" tab in a GitHub repository?
15. How do you close an issue on GitHub?


Answers:

1.GitHub is a web-based platform for version control and collaborative software development. It allows individuals and teams to host, manage, and share code repositories.

2.To create a GitHub account, visit the GitHub website (https://github.com) and click on the "Sign up" button. You'll need to provide your email address, choose a username, and create a password.

3.A repository in GitHub is a location where you can store and manage your code and project files. It can be thought of as a folder for your project, including version history and collaborative tools.

4.To create a new repository on GitHub, follow these steps:

Log in to your GitHub account.
Click on the "+" icon in the top-right corner and select "New repository."
Provide a repository name, description, and other settings.
Click the "Create repository" button.

5.A README.md file is a Markdown-formatted document that provides an introduction and documentation for your project. It's displayed on your GitHub repository's main page and is important for explaining your project's purpose and how to use it. 

6.To add files to a GitHub repository, you can use the web interface or Git commands like git add and git commit. 
for example:
git add robin.txt
git commit -m "Add robin.txt"

7.You can commit changes to a repository in GitHub using Git commands like git commit and git push. 
for example:
git commit -m "Updated code"
git push

8.A pull request is a way to propose changes to a repository. You can create one by:
.Forking the repository you want to contribute to.
.Creating a new branch for your changes.
.Making your changes and committing them.
.Opening a pull request from your branch to the original repository.

9.A fork in GitHub is a personal copy of another user's repository. It allows you to make changes independently of the original repository. You can fork a repository using the "Fork" button on the repository's page.

10.To clone a repository to your local machine, use the "git clone" command followed by the repository's URL. For example:
git clone https://github.com/robin/robin-repo.git

11.To push changes from your local machine to a GitHub repository, use the "git push" command. For example:
git push origin master

12.A branch in GitHub is a parallel version of the main codebase. You would use branches to work on new features, bug fixes, or experiments without affecting the main/master branch.

13.To merge a branch into the main/master branch, create a pull request and, after review and approval, use the "Merge" button on the pull request page.

14.The "Issues" tab in a GitHub repository is used to track and manage tasks, enhancements, and bugs related to the project. It's a place for collaboration and discussion.

15.To  close an issue on GitHub, open the issue, and then click the "Close issue" button or comment with a keyword like "closes" or "fixes" followed by the issue number. For example
Closes #3