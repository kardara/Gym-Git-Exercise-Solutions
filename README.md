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





 ```

#Here is my other repository that i have worked on
https://github.com/kardara/Gym-Git-Exercise-Bundle1.git  
