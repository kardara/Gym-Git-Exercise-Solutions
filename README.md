```bash
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
 ```

#Here is my other repository that i have worked on
https://github.com/kardara/Gym-Git-Exercise-Bundle1.git  
