```bash
Bundle 1
#Exercise 1

# Create folder and initialize git
`mkdir thegymgit` #Creates a new directory (folder) named thegymgit where your project files will reside.
`cd thegymgit` #Navigates into the thegymgit directory so you can work inside it
`git init` #Initializes a new Git repository in the current directory. This creates a hidden .git folder where Git stores all its tracking data for version control.

# Add files and contents
# Rename branch
`git branch -m main`  # Rename from master to main. By default, Git used to name the main branch as master

# Stage and commit changes
`git add .` #Stages all changes (files and modifications) in your working directory. Staging means you’re preparing them for inclusion in the next commit.
`git commit -m "Initial commit with project files"`

# Connect to GitHub
`git remote add origin https://github.com/kardara/Gym-Git-Exercise-Bundle1.git  `
`git push -u origin main` #Pushes your local main branch to the main branch on the GitHub remote repository.The -u flag sets this remote branch as the default, so future pushes or pulls will automatically target origin main.

# Create new branches
`git checkout -b dev` #Creates a new branch named dev and switches to it. The dev branch is often used for development work to keep the main branch clean.
`git checkout -b test` #Creates another branch named test from the dev branch. This branch could be used for testing features.

# Delete test branch
`git checkout dev` #Switches back to the dev branch.
`git branch -d test` #Deletes the test branch. The -d flag ensures the branch is safely deleted only if it has been fully merged into another branch (like dev).

Exercise 1

`git add home.html ` # Stage the home.html file
`git stash save "Adding home.html changes"`  # Save changes to stash
Output: Saved working directory and index state On main: Adding home.html
`git add about.html ` # Stage the about.html file
`git stash save "Adding about.html changes"`  # Save changes to stash
Output: Saved working directory and index state On main: Adding about.html
`git add team.html ` # Stage the team.html file
`git stash save "Adding team.html changes"`  # Save changes to stash
Output: Saved working directory and index state On main: Adding team.html
`git stash pop "stash@{1}"` # Apply and remove stash for about.html
Output: On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Home.html
        team.html

Dropped stash@{1} (4cf53a0fb3063927fb372c1048b28d173b1763f5)

`git stash pop "stash@{2}"` # Apply and remove stash for home.html
Output: On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

Dropped stash@{2} (521e8d7782f17bc67045e5bef4b067d1e25655e0)

`git add . ` # Stage all changes
`git commit -m "Restore home.html and about.html changes"` #Commit changes
Output: [main 75d6098] Restore home.html and about.html changes
 3 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 team.html

`git push origin` #Pushing all the changes
Output: Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 651 bytes | 651.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/kardara/Gym-Git-Exercise-Bundle1.git
   ba7b8fc..75d6098  main -> main

`git stash pop` # Apply and remove the latest stash for team.html
Output: Auto-merging team.html
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
Dropped refs/stash@{0} (b7a99feb3226fa1c3baf15c31fed6a5c7ed45584)

`git reset --hard HEAD` # Reset the working directory to the last commit
Output: HEAD is now at 75d6098 Restore home.html and about.html changes


Bundle 1
#Exercise 1
`git checkout -b ft/bundle-2` #Create a new branch ft/bundle-2
OutPut: Switched to a new branch 'ft/bundle-2'

`git status` #Checking the status
Output: On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        service.html

nothing added to commit but untracked files present (use "git add" to track)

#Commit the changes
`git add service.html` 
`git commit -m "Add service page"`
Output: [ft/bundle-2 ffed561] Add service page
 1 file changed, 11 insertions(+)
 create mode 100644 service.html

`git push origin ft/bundle-2` #Push the changes to github
Output: Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 437 bytes | 437.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/kardara/Gym-Git-Exercise-Bundle1/pull/new/ft/bundle-2
remote:
To https://github.com/kardara/Gym-Git-Exercise-Bundle1.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

 #Exercise 2

 #Checkout the main branch and pull the latest changes
 `git checkout main`
 OUtput: Switched to branch 'main'
Your branch is up to date with 'origin/main'.

`git pull origin main`
Output: remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 905 bytes | 90.00 KiB/s, done.
From https://github.com/kardara/Gym-Git-Exercise-Bundle1
 * branch            main       -> FETCH_HEAD
   75d6098..f900422  main       -> origin/main
Updating 75d6098..f900422
Fast-forward
 service.html | 11 +++++++++++
 1 file changed, 11 insertions(+)
 create mode 100644 service.html

#Create a new branch ft/service-redesign
 `git checkout -b ft/service-redesign`
Output: Switched to a new branch 'ft/service-redesign'

#Commit and push the changes
`git add service.html`
`git commit -m "Redesign the services page"`
Output: [ft/service-redesign 981b87c] Redesign the services page
 1 file changed, 1 insertion(+)
PS C:\Users\USER\Desktop\Git_Exercises\Gym-Git-Exercise-Bundle1> git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 384 bytes | 192.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/kardara/Gym-Git-Exercise-Bundle1/pull/new/ft/service-redesign
remote:
To https://github.com/kardara/Gym-Git-Exercise-Bundle1.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

#Compare the ft/service-redesign branch with main to observe differences
`git diff main..ft/service-redesign`
output: diff --git a/service.html b/service.html
index 05fc9e8..9bca037 100644
--- a/service.html
+++ b/service.html
@@ -7,6 +7,6 @@
 </head>
 <body>
     <h1>Welcome to Service page</h1>
-    <p>This is for the main branche</p>

#Merge the main branch into ft/service-redesign
`git merge main`
Output: Updating 981b87c..89ae5e8
Fast-forward
 service.html | 4 ++++
 1 file changed, 4 insertions(+)

#Commit and push the resolved changes
`git add service.html`
`git commit -m "Merge main into ft/service-redesign and resolve conflicts"`
`git push origin ft/service-redesign`
OUtput: On branch ft/service-redesign
nothing to commit, working tree clean
PS C:\Users\USER\Desktop\Git_Exercises\Gym-Git-Exercise-Bundle1> git push origin ft/service-redesign
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/kardara/Gym-Git-Exercise-Bundle1.git
   981b87c..89ae5e8  ft/service-redesign -> ft/service-redesign


 Bundle 3
# Exercise 1

# Create and switch to a new branch `ft/team-page`
`git checkout -b ft/team-page`

# Add a new file and commit changes
`git add team.html`
`git commit -m "Add team page"`
Output: [ft/team-page 658be3a] Add team page
 1 file changed, 1 insertion(+)

# Push changes and create a pull request (PR)
`git push origin ft/team-page`
Output: Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 333 bytes | 166.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/kardara/Gym-Git-Exercise-Bundle1/pull/new/ft/team-page
remote:
To https://github.com/kardara/Gym-Git-Exercise-Bundle1.git
 * [new branch]      ft/team-page -> ft/team-page

# Switch back to `main` branch
`git checkout main`

# Create a new branch `ft/contact-page`
git checkout -b ft/contact-page

# Switch to `ft/team-page` and copy the last commit hash
git checkout ft/team-page
git log --oneline  # Copy the last commit hash
Output: 658be3a (HEAD -> ft/team-page, origin/ft/team-page) Add team page
89ae5e8 (origin/main, origin/ft/service-redesign, origin/HEAD, main, ft/service-redesign, ft/contact-page) Resolve merge conflicts with remote main
f73d9f2 Fix services page
622f447 Merge pull request #2 from kardara/ft/service-redesign
981b87c Redesign the services page
f900422 Merge pull request #1 from kardara/ft/bundle-2
ffed561 (origin/ft/bundle-2, ft/bundle-2) Add service page
75d6098 Restore home.html and about.html changes

# Switch back to `ft/contact-page` and cherry-pick the commit
`git checkout ft/contact-page`
`git cherry-pick 658be3a`
Output: [ft/contact-page 0600108] Add team page
 Date: Sat Jan 4 19:58:15 2025 +0200
 1 file changed, 1 insertion(+)

 # Add changes for the contact page
`git add contact.html`
`git commit -m "Add contact page"`
`git push origin ft/contact-page`

# Create a new branch `ft/faq-page` from `ft/contact-page`
`git checkout -b ft/faq-page`

# Add and commit changes for the FAQ page
`git add faq.html`
`git commit -m "Add FAQ page"`
`git push origin ft/faq-page`

# Revert the last commit of `ft/team-page` and push changes
`git checkout ft/team-page`
Output: M       about.html
        M       service.html
Switched to branch 'ft/team-page'

`git revert 658be3a`  # Use the copied hash from the `ft/team-page` commit
Output: [ft/team-page 8f00b1a] Revert "Add team page"
 1 file changed, 1 deletion(-)

`git push origin ft/team-page`
Output: Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 321 bytes | 107.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/kardara/Gym-Git-Exercise-Bundle1.git
   658be3a..8f00b1a  ft/team-page -> ft/team-page

#Exercise 2
# Create a new branch `ft/home-page-redesign` from `ft/faq-page`
`git checkout -b ft/home-page-redesign`

# Go back to `main` and make changes
`git checkout main`
`git add index.html`
`git commit -m "Update home page"`
`git push origin main`

# Rebase `ft/home-page-redesign` to `main`
`git checkout ft/home-page-redesign`
`git rebase main`
Output: Successfully rebased and updated refs/heads/ft/home-page-redesign.

# Add changes to the home page and commit
`git add index.html`
`git commit -m "Redesign home page"`
`git push origin ft/home-page-redesign`
Output: Enumerating objects: 21, done.
Counting objects: 100% (21/21), done.
Delta compression using up to 8 threads
Compressing objects: 100% (16/16), done.
Writing objects: 100% (16/16), 1.74 KiB | 148.00 KiB/s, done.
Total 16 (delta 9), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (9/9), completed with 3 local objects.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/kardara/Gym-Git-Exercise-Bundle1/pull/new/ft/home-page-redesign
remote:
To https://github.com/kardara/Gym-Git-Exercise-Bundle1.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign


 Bundle 4

 #Exercise 1
 `git checkout main` # checkout the main branch
`git remote add git-copy https://github.com/kardara/gym-git-exercise-copy.git` #Add the Repository as a Second Remote

#Commit the Changes
`git add index.html`
`git commit -m "Updated the home page"`

#Push Changes to Both Remotes
`git push origin main`
Output: Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 346 bytes | 69.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/kardara/Gym-Git-Exercise-Bundle1.git
   7593b4f..1cfeccb  main -> main

`git push git-copy main`
Output: Enumerating objects: 33, done.
Counting objects: 100% (33/33), done.
Delta compression using up to 8 threads
Compressing objects: 100% (30/30), done.
Writing objects: 100% (33/33), 4.73 KiB | 255.00 KiB/s, done.
Total 33 (delta 17), reused 7 (delta 2), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (17/17), done.
To https://github.com/kardara/gym-git-exercise-copy.git
 * [new branch]      main -> main


#Exercise 2
`git checkout -b ft/footer` # git checkout -b ft/footer
# Add Changes and Commit Them
`git add .`
`git commit -m "Added footer section"`
#Add More Changes and Create a Second Commit
`git add .`
`git commit -m "Updated footer styles"`
#Push and Create a New PR
`git push origin ft/footer`
# Checkout the main Branch Again
`git checkout main`
#Create a New Branch Named ft/squashing
`git checkout -b ft/squashing`
#Merge Squash the Changes on the ft/footer Branch
`git merge --squash ft/footer`
Output: Updating 1cfeccb..dca7024
Fast-forward
Squash commit -- not updating HEAD
 contact.html | 12 ++++++++++++
 faq.html     | 12 ++++++++++++
 home.html    |  1 +
 index.html   |  1 +
 service.html |  5 +----
 team.html    |  1 +
 6 files changed, 28 insertions(+), 4 deletions(-)
 create mode 100644 contact.html
 create mode 100644 faq.html

#Commit the Squashed Changes
`git commit -m "footer changes squashing"`
Output: [ft/squashing e4352e7] footer changes squashing
 6 files changed, 28 insertions(+), 4 deletions(-)
 create mode 100644 contact.html
 create mode 100644 faq.html

#Push the Changes and Create a PR
`git push origin ft/squashing`


 ```

#Here is my other repository that i have worked on
https://github.com/kardara/Gym-Git-Exercise-Bundle1.git  
