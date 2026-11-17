# To document all errors and fixes
# Issues encountered while commiting to GitHUb:
all the staged changes list is already in the GitHub under the repository under main branch. It was committed initially when the repo was private. Now, the repo is changed from private to public and changes from the first commit is still in the main -looks ok. But VS code still shows all 5 files to be committed

Your screenshot shows all 5 files marked with a green A (Added) under Staged Changes. This happens because your local VS Code repository is out of sync with the remote history on GitHub—likely because you previously clicked Undo Last Commit locally after already pushing, or your local branch hasn't fetched the latest state from origin/main

Soln:git fetch origin

fatal: 'origin' does not appear to be a git repository. This happens because your local folder (hotel_guest_exp_dw) is not linked to your GitHub repository URL yet—which also explains why VS Code thinks all 5 files are brand new and ready for an initial commit.
Soln: git reset --hard origin/main