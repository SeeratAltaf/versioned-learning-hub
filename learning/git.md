# Git Notes
# git add . - It stages all new, modified, and deleted files in the current directory and everything inside it for the next commit.

# git commit takes everything you staged (git add ...) and locks it into Git history as a snapshot.
git commit -m "message"
commit → create a snapshot
-m → message
"message" → explains what changed and why
When you run git commit:

Git takes the staging area

Creates a snapshot (commit)

Assigns it:

a unique hash (ID)

author

timestamp

message

Stores it locally (NOT GitHub)
# Connect local → GitHub
git remote add origin https://github.com/YOUR_USERNAME/versioned-learning-hub.git

# git remote -v
shows which remote repositories your local Git project is connected to and where they point.
origin → default nickname for the remote repo
fetch → where Git pulls code from
push → where Git sends code to

# git push -u origin main
usually your first-ever push, Push my local main branch to origin, and remember this link.
-u → set upstream (this is the key part)
after this simply do "git push"

# git switch -c feature/git-notes
“This work is optional until approved.”

Push the feature branch to GitHub
git push -u origin feature/git-notes

Now GitHub has this branch. main is untouched.
A branch is not “a version of files”
A branch is “a timeline of commits”

Files appear under a branch only because they changed in that timeline.
Branches don’t contain files — they contain commits.

ou already had main on GitHub
→ This is the stable, official branch.

You created a new branch locally
→ Purpose: work safely without touching main.

You made changes on that branch
→ Feature work / learning notes / improvements.

You decided the changes were good
→ This is the human decision point.

You pushed the branch to GitHub
→ So GitHub can see it (backup + review).

You opened a Pull Request (PR)
→ Meaning: “I propose merging this work into main.”

You merged the PR on GitHub
→ This officially applied your changes to main.

You deleted the branch
→ Clean-up. The work is done; the branch has no purpose
git switch main
git pull

This syncs your laptop with GitHub’s updated main.