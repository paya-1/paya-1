- 👋 Hi, I’m @paya-1
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---














































































mkdir git_s
cd git_se
git init
vi file.txt
git status
git add file.txt
git status
git commit-m "my first commit"

git config --global user.name""
git config --global user.email""
git commit --m"my first commit"
git log 
git branch
git checkout master
git merge feature_branch
git_branch

git stash save "updated file"
git checkout  master
git stash apply
git clone 
git fetch origin
git push origin new_branch
git branch
git merge new_branch -m
     merging new branch master -o master



























$ git init
3. Create a new file in the directory. For example, let's create a file named "my_file.txt."
You can use any text editor or command-line tools to create the file.
4. Add the newly created file to the staging area. Replace "my_file.txt" with the actual
name of your file:
$ git add my_file.txt
This command stages the file for the upcoming commit.
5. Commit the changes with an appropriate commit message. Replace "Your commit
message here" with a meaningful description of your changes:
$ git commit -m "Your commit message here"
Your commit message should briefly describe the purpose or nature of the changes you made.
For example:
$ git commit -m "Add a new file called my_file.txt"
13
After these steps, your changes will be committed to the Git repository with the provided
commit message. You now have a version of the repository with the new file and its history
stored in Git.
Experiment 2.
Creating and Managing Branches:
14
Create a new branch named "feature-branch." Switch to the "master" branch.
Merge the"feature-branch" into "master."
Solution:
To create a new branch named "feature-branch," switch to the "master" branch, and merge the
"feature-branch" into "master" in Git, follow these steps:
1. Make sure you are in the "master" branch by switching to it:
$ git checkout master
2. Create a new branch named "feature-branch" and switch to it:
$ git checkout -b feature-branch
This command will create a new branch called "feature-branch" and switch to it.
3. Make your changes in the "feature-branch" by adding, modifying, or deleting files as
needed.
4. Stage and commit your changes in the "feature-branch":
$ git add .
$ git commit -m "Your commit message for feature-branch"
Replace "Your commit message for feature-branch" with a descriptive commit message for the
changes you made in the "feature-branch."
5. Switch back to the "master" branch:
$ git checkout master
6. Merge the "feature-branch" into the "master" branch:
$ git merge feature-branch
This command will incorporate the changes from the "feature-branch" into the "master" branch.
Now, your changes from the "feature-branch" have been merged into the "master" branch. Your
project's history will reflect the changes made in both branches
Experiment 3.
Creating and Managing Branches:
15
Write the commands to stash your changes, switch branches, and then apply the
stashedchanges.
Solution:
To stash your changes, switch branches, and then apply the stashed changes in Git, you can use
the following commands:
1. Stash your changes:
$ git stash save "Your stash message"
This command will save your changes in a stash, which acts like a temporary storage for
changes that are not ready to be committed.
2. Switch to the desired branch:
$ git checkout target-branch
Replace "target-branch" with the name of the branch you want to switch to.
3. Apply the stashed changes:
$ git stash apply
This command will apply the most recent stash to your current working branch. If you have
multiple stashes, you can specify a stash by name or reference (e.g., git stash apply stash@{2})
if needed.
If you want to remove the stash after applying it, you can use git stash pop instead of git stash
apply.
Remember to replace "Your stash message" and "target-branch" with the actual message you
want for your stash and the name of the branch you want to switch to.
Experiment 4.
Collaboration and Remote Repositories:
16
Clone a remote Git repository to your local machine.
Solution:
To clone a remote Git repository to your local machine, follow these steps:
1. Open your terminal or command prompt.
2. Navigate to the directory where you want to clone the remote Git repository. You can
use the cd command to change your working directory.
3. Use the git clone command to clone the remote repository. Replace <repository_url>
with the URL of the remote Git repository you want to clone. For example, if you were
cloning a repository from GitHub, the URL might look like this:
$ git clone <repository_url>
Here's a full example:
$ git clone https://github.com/username/repo-name.git
Replace https://github.com/username/repo-name.git with the actual URL of the repository you
want to clone.
4. Git will clone the repository to your local machine. Once the process is complete, you
will have a local copy of the remote repository in your chosen directory.
You can now work with the cloned repository on your local machine, make changes, and push
those changes back to the remote repository as needed.
17
Experiment 5.
Collaboration and Remote Repositories:
Fetch the latest changes from a remote repository and rebase your local branch onto
the updated remote branch.
Solution:
To fetch the latest changes from a remote repository and rebase your local branch onto the
updated remote branch in Git, follow these steps:
1. Open your terminal or command prompt.
2. Make sure you are in the local branch that you want to rebase. You can switch to the
branch using the following command, replacing <branch-name> with your actual
branch name:
$ git checkout <branch-name>
3. Fetch the latest changes from the remote repository. This will update your local
repository with the changes from the remote without merging them into your local
branch:
$ git fetch origin
Here, origin is the default name for the remote repository. If you have multiple remotes, replace
origin with the name of the specific remote you want to fetch from.
4. Once you have fetched the latest changes, rebase your local branch onto the updated
remote branch:
$ git rebase origin/<branch-name>
Replace <branch-name> with the name of the remote branch you want to rebase onto. This
command will reapply your local commits on top of the latest changes from the remote branch,
effectively incorporating the remote changes into your branch history.
5. Resolve any conflicts that may arise during the rebase process. Git will stop and notify
you if there are conflicts that need to be resolved. Use a text editor to edit the conflicting
files, save the changes, and then continue the rebase with:
$ git rebase --continue
18
6. After resolving any conflicts and completing the rebase, you have successfully updated
your local branch with the latest changes from the remote branch.
7. If you want to push your rebased changes to the remote repository, use the git push
command. However, be cautious when pushing to a shared remote branch, as it can
potentially overwrite other developers' changes:
$ git push origin <branch-name>
Replace <branch-name> with the name of your local branch. By following these steps, you can
keep your local branch up to date with the latest changes from the remote repository and
maintain a clean and linear history through rebasing.
Experiment 6.
19
Collaboration and Remote Repositories:
Write the command to merge "feature-branch" into "master" while providing a custom
commit message for the merge.
Solution:
To merge the "feature-branch" into "master" in Git while providing a custom commit message
for the merge, you can use the following command:
$ git checkout master
$ git merge feature-branch -m "Your custom commit message here"
Replace "Your custom commit message here" with a meaningful and descriptive commit
message for the merge. This message will be associated with the merge commit that is created
when you merge "feature-branch" into "master."
Experiment 7.
1
10
Git Tags and Releases:
Write the command to create a lightweight Git tag named "v1.0" for a commit in your
local repository.
Solution:
To create a lightweight Git tag named "v1.0" for a commit in your local repository, you can
use the following command:
$ git tag v1.0
This command will create a lightweight tag called "v1.0" for the most recent commit in your
current branch. If you want to tag a specific commit other than the most recent one, you can
specify the commit's SHA-1 hash after the tag name. For example:
$ git tag v1.0 <commit-SHA>
Replace <commit-SHA> with the actual SHA-1 hash of the commit you want to tag.
Experiment 8.
1
11
Advanced Git Operations:
Write the command to cherry-pick a range of commits from "source-branch" to the
current branch.
Solution:
To cherry-pick a range of commits from "source-branch" to the current branch, you can use
the following command:
$ git cherry-pick <start-commit>^..<end-commit>
Replace <start-commit> with the commit at the beginning of the range, and <end-commit>
with the commit at the end of the range. The ^ symbol is used to exclude the <start-commit>
itself and include all commits after it up to and including <end-commit>. This will apply the
changes from the specified range of commits to your current branch.
For example, if you want to cherry-pick a range of commits from "source-branch" starting from
commit ABC123 and ending at commit DEF456, you would use:
$ git cherry-pick ABC123^..DEF456
Make sure you are on the branch where you want to apply these changes before running the
cherry-pick command.
Experiment 9.
20
Analysing and Changing Git History:
Given a commit ID, how would you use Git to view the details of that specific commit,
including the author, date, and commit message?
Solution:
To view the details of a specific commit, including the author, date, and commit message, you
can use the git show or git log command with the commit ID. Here are both options:
1. Using git show:
bash
git show <commit-ID>
Replace <commit-ID> with the actual commit ID you want to view. This command will display
detailed information about the specified commit, including the commit message, author, date,
and the changes introduced by that commit.
For example:
$ git show abc123
2. Using git log:
$ git log -n 1 <commit-ID>
The -n 1 option tells Git to show only one commit. Replace <commit-ID> with the actual
commit ID. This command will display a condensed view of the specified commit, including
its commit message, author, date, and commit ID.
For example:
$ git log -n 1 abc123
Both of these commands will provide you with the necessary information about the specific
commit you're interested in

     
