Answer 1 --global tells Git to save the name and email settings for all repositories on this computer. If I don't use it, the settings will apply only to the current repository, provided it is already initialized.	

Answer 2 The entries ., .., .git, and .venv appeared when I used ls -a because this command also shows hidden files and folders. The .git folder stores the repository's data, settings, and commit history.

Answer 3 Git is offering to track around 4 files and folders: week02/lab01-log.txt, week02/notes.md, README.md, and the lab4 folder. The lab4 folder is noteworthy because it may contain files I did not write myself, depending on what is inside it.

Answer 4 Compared to the previous git status, the .venv/ folder has disappeared because it is now being ignored by Git using .gitignore. The .gitignore file itself is now showing under Untracked files because it has not been added to Git yet.

Answer 5 Yes, .gitignore should be committed. It contains the rules for which files Git should ignore, so committing it makes sure everyone working on the project follows the same rules.

Answer 6 README.md moved from Untracked files to Changes to be committed. In the three-places model, this means README.md was moved from the Working Directory to the Staging Area by using git add.

Answer 7 After the commit, Git printed Lab work so far and showed that 5 files changed, with 175 insertions. It also listed the five files that were created in the commit.

Answer 8  The first seven characters, 9494405, are called the short commit hash. They are used as a unique ID to identify a particular commit in Git history.

Answer 9 
