# README #


Pushing Repo to GitHub

1. Create a new Repository in GitHub website.
2. Open terminal in Macbook.
3. Type PWD in terminal.
4. Type 'cd' and locate the folder which one need to push in GitHub. Example: cd /Users/ferdous/eclipse-workspace
5. Initialize GitHub by typing, 
	'git init'
6. Type 'git add .' It will add all files which will upload.
6a. Use 'git rm --cached <file>...' to unstage.
7. Type 'git status' it will show your files that will upload.
8. Type 'git commit -u "This is first commit" '
9. Type 'git remote add origin <url of the created new repository>'
10. Type 'git push -u origin master'
11. GitHub will ask your username and Password.

Username of gitHub: ferdousbhuiya
Password: the token from gitHub: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


SSH Key:
MacBookPro
SHA256:7jFxwHhQmFwOG1BzkPA7I5S60mDQvQX3F2MH+HPrnEk
Added on Sep 25, 2022
Never used — Read/write


Testing your SSH connection:
Open Terminal.

Enter the following:  ssh -T git@github.com
Enter 'yes'


********************** ========================== *********************


To make a Git useable directory (folder):
First of all go to that folder by commanding in terminal. 

$ cd <path of the folder>

Example: 

MacBook-Pro:~ ferdous$ cd /Users/ferdous/IdeaProjects/git_basics

After the cd is the folder path </Users/ferdous/IdeaProjects/git_basics>
Then in terminal command, git init then enter

Example: MacBook-Pro:git_basics ferdous$ git init

It will show: Initialized empty Git repository in /Users/ferdous/IdeaProjects/git_basics/.git/
MacBook-Pro:git_basics ferdous$ 

In the folder there will be a hidden folder (.git).

In terminal we can type : git status
That will show our files which was not committed or uploaded. 

Result: On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	LICENSE.md
	README.md

nothing added to commit but untracked files present (use "git add" to track)
MacBook-Pro:git_basics ferdous$ 

To add all files in the gitHub:
There are two commands: git add --all or git add .

After then it will show:

On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   LICENSE.md
	new file:   README.md

MacBook-Pro:git_basics ferdous$ 

Now it is ready to commit.

For commiting:

git commit -m "This is first commit for this test project."

That will show this result:

[master (root-commit) b0ea141] First Commit
 2 files changed, 2 insertions(+)
 create mode 100644 LICENSE.md
 create mode 100644 README.md
MacBook-Pro:git_basics ferdous$ 

git log            will show you the all activities

MacBook-Pro:git_basics ferdous$ git log
commit b0ea1410ea13e68d699670a0fc2562bbab3ade5d (HEAD -> master)
Author: ferdousbhuiya <ferdousbhuiya@gmail.com>
Date:   Sat Oct 1 21:28:42 2022 -0400

    First Commit
You have new mail in /var/mail/ferdous
MacBook-Pro:git_basics ferdous$ 

If we want to see the log in short space we have to use : git log --oneline

The result is like this:

MacBook-Pro:git_basics ferdous$ git log --oneline
b0ea141 (HEAD -> master) First Commit
MacBook-Pro:git_basics ferdous$ 


Both are the same but in shorter space. 

I have some changed in "README" file and made commit like these steps.

MacBook-Pro:git_basics ferdous$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
MacBook-Pro:git_basics ferdous$ git add .
MacBook-Pro:git_basics ferdous$ git commit -m "How are you added"
[master e753d82] How are you added
 1 file changed, 1 insertion(+)
MacBook-Pro:git_basics ferdous$ 


We have already changed to the file and committed but if we feel that we will not save the changes in that file, at that time we have to command in the terminal:

It will show like this and the new lines will be removed from the file.

MacBook-Pro:git_basics ferdous$ git checkout b0ea141
Previous HEAD position was e753d82 How are you added
HEAD is now at b0ea141 First Commit
MacBook-Pro:git_basics ferdous$ 

We have to put the number after checkout, here the number is " b0ea141 ".
If we would like to go to any stage then we have to know the commit number. 


If we want to go back to the main branch before checkout then we can go the main commit. Then we can see all in the previous condition. 


Output:

MacBook-Pro:git_basics ferdous$ git checkout master
Previous HEAD position was b0ea141 First Commit
Switched to branch 'master'
MacBook-Pro:git_basics ferdous$


To see the difference between commit , we can type the command: git diff

MacBook-Pro:git_basics ferdous$ git diff

The output is like this:

diff --git a/README.md b/README.md
index 1fbd1eb..4359670 100644
--- a/README.md
+++ b/README.md
@@ -1,2 +1,4 @@
 # README #
-Hello how are you
\ No newline at end of file
+Hello how are you
+
+I am fine.
\ No newline at end of file
MacBook-Pro:git_basics ferdous$ 