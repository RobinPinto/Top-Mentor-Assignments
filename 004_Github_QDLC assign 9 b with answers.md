## Github_QDLC(L4)

**Push, Commit, Add:**

1. What does the "git add" command do in Git?
2. How do you stage changes for a commit in Git?
3. What is a Git commit, and how is it different from a push?
4. How can you create a Git commit with a commit message?
5. What does "git push" do in Git, and why is it important?
6. How do you push your local Git commits to a remote repository?
7. Can you explain the difference between "git add" and "git commit"?

**Config:**

8. What is the purpose of Git configuration settings?
9. How do you set your Git username and email globally?
10. What is the difference between local and global Git configurations?
11. How can you view your Git configuration settings?
12. Why is it important to configure your Git identity?

**Merge, Pull, Branch:**

13. What is a Git branch, and why do we use them?
14. How do you create a new Git branch?
15. What is the "git merge" command used for in Git?
16. How do you merge changes from one branch into another?
17. What is a merge conflict, and how can you resolve it?
18. What is the purpose of the "git pull" command in Git?
19. How do you update your local repository with changes from a remote repository using "git pull"?
20. Can you explain the difference between "git merge" and "git pull"?

**General Git:**

21. What is Git, and what problem does it solve in software development?
22. How do you initialize a Git repository in a directory?
23. How do you check the status of your Git repository?
24. What is the purpose of the ".gitignore" file in Git?
25. How can you view the commit history of a Git repository?
26. How do you create a new Git repository on a remote hosting service like GitHub or GitLab?
27. What is the purpose of a Git remote?
28. How can you add a remote repository to your local Git repository?
29. What is the Git workflow for making changes, committing, and pushing to a remote repository?
30. How do you undo the last Git commit?


Answers:


**Push, Commit, Add:**

1.What does the "git add" command do in Git?

git add is used to stage changes for a commit in Git. It prepares files to be included in the next commit.

2.How do you stage changes for a commit in Git?

Use git add followed by the filename or directory to stage changes. For example: git add file.txt.

3.What is a Git commit, and how is it different from a push?

A Git commit records the changes you've staged in your local repository, creating a snapshot of the code at that point. It's different from a push, which uploads your commits to a remote repository (e.g., GitHub).

4.How can you create a Git commit with a commit message?

Use git commit -m "Your commit message" to create a commit with a descriptive message that explains the changes made.

5.What does "git push" do in Git, and why is it important?

git push is used to upload your local Git commits to a remote repository, making them accessible to others. It's essential for collaboration and code sharing.

6.How do you push your local Git commits to a remote repository?

After making local commits, use git push followed by the remote repository's name (e.g., "origin") and the branch name to upload your changes. For example: git push origin main.

7.Can you explain the difference between "git add" and "git commit"?

git add stages changes for the next commit but doesn't create a commit. It prepares files to be included in a commit.
git commit creates a snapshot of the staged changes, along with a commit message, and records it in your local repository. It makes your changes permanent in your local history.


**Config:**

8.What is the purpose of Git configuration settings?

Git configuration settings control various aspects of how Git operates, including user identity, default behavior, aliases, and more.

9.How do you set your Git username and email globally?

To set your Git username and email globally, you can use the following commands:
git config --global user.name "Your Name"
git config --global user.email "your@email.com"

10.What is the difference between local and global Git configurations?

Local Git configurations apply to a specific repository, while global configurations apply to all Git repositories on your machine. Local settings override global settings if there is a conflict.

11.How can you view your Git configuration settings?

You can view your Git configuration settings using the git config command with options like --list to display all settings or --global to see global settings. For example:
git config --list

12.Why is it important to configure your Git identity?

Configuring your Git identity (name and email) is important because it associates your commits with your identity. It helps collaborators and tools attribute code contributions to you, making it easier to track changes and contributions in a project's history.

**Merge, Pull, Branch:**

13.What is a Git branch, and why do we use them?

A Git branch is a separate line of development that allows you to work on features, bug fixes, or experiments without affecting the main code. Branches help in collaborative and organized development.

14.How do you create a new Git branch?

To create a new branch, use the git checkout -b command followed by the branch name. For example: git checkout -b feature-branch.

15.What is the "git merge" command used for in Git?

The git merge command is used to combine changes from one branch into another, typically merging a feature or bug-fix branch into the main/master branch.

16.How do you merge changes from one branch into another?

To merge changes from one branch into another, use git merge while on the target branch. For example, to merge changes from a feature branch into the main branch: git checkout main and git merge feature-branch.

17.What is a merge conflict, and how can you resolve it?

A merge conflict occurs when Git is unable to automatically merge changes from different branches. To resolve it, you need to manually edit the conflicting files, then commit the changes. After resolving, use git commit to finalize the merge.

18.What is the purpose of the "git pull" command in Git?

git pull is used to fetch changes from a remote repository and merge them into your current branch, keeping your local repository up to date with the remote.

19.How do you update your local repository with changes from a remote repository using "git pull"?

Simply run git pull while in your local repository. Git will fetch and merge the changes from the remote branch into your current local branch.

20.Can you explain the difference between "git merge" and "git pull"?

git merge is used to combine changes from one branch into another, while git pull is used to fetch and merge changes from a remote repository into your current branch. Essentially, git pull is a combination of git fetch and git merge for remote updates.

**General Git:**

21.What is Git, and what problem does it solve in software development?

Git is a distributed version control system. It solves the problem of tracking and managing changes in software development, enabling collaboration, version history, and code synchronization among developers.

22.How do you initialize a Git repository in a directory?

Use the git init command to initialize a new Git repository in a directory.

23.How do you check the status of your Git repository?

Use the git status command to see the current status of your Git repository, including untracked, modified, and staged files.

24.What is the purpose of the ".gitignore" file in Git?

The ".gitignore" file specifies files or directories that Git should ignore, preventing them from being tracked or committed. It's useful for excluding build artifacts, temporary files, and sensitive data from version control.

25.How can you view the commit history of a Git repository?

Use the git log command to view the commit history, displaying details about each commit, including the author, date, and commit message.

26.How do you create a new Git repository on a remote hosting service like GitHub or GitLab?

Sign in to your hosting service, e.g., GitHub or GitLab.
Click "New repository" and follow the instructions to create a remote repository.

27.What is the purpose of a Git remote?

A Git remote is a reference to a repository hosted on a server. It allows you to interact with and exchange data with remote repositories.

28.How can you add a remote repository to your local Git repository?

Use the git remote add command, providing a name for the remote and its URL. For example: git remote add origin https://github.com/username/repo.git.

29.What is the Git workflow for making changes, committing, and pushing to a remote repository?
Make changes, stage them with git add, commit with git commit, and push to a remote repository with git push.

30.How do you undo the last Git commit?
Use git reset HEAD~1 to undo the last commit while keeping your changes in the working directory. Use caution, as this reverts the commit but retains changes as uncommitted.