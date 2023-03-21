
# TD4

## Exercise 1

### 3. Using only command-line in your Linux shell, clone it to a local repository.
```
git clone https://github.com/TkCode1/td4gitbranches
```
## Exercise 2

### Using only the shell in your local repository :
### 1. Create a branch named after you.
```
cd td4gitbranches
git branch <branche>
```
### 2. Create a new text file named after you (with the content you want).
```
git checkout <branche>
echo > nom.txt
```
### 3. Commit this new file.
```
git add nom.txt 
git commit -m "Ajout de mon fichier nom.txt"
```
### 4. Push your branch to the remote repository.
```
git push -u origin <branche>
```
## Exercise 3

### Using only the shell :
### 1. Merge your branch into the ’master’ branch.
```
git checkout main
git merge <branch>
```
### 2. Push your changes in the ’master’ branch to the remote repositor
```
git push origin <branche>
```

## Exercise 4

### For the repository owner... In the web UI, make sure lines 2 to 6 of the
README.md are not empty.
One person at a time, using only the shell :
### 1. Switch back to your own branch (not including the latest changes from
the master branch).
### 2. Edit the lines 2 to 6 of the README.md file with a text you like (a
poem, a quote, some clever code...). It can be any readable text, it may
be incomplete, it must just take about 5 lines and be different from your
teammates. It must start on line 2 to trigger conflicts between team
members.
### 3. Commit this change.
### 4. Pull latest status from the remote repository ’master’ branch into your
local ’master’ branch.
### 5. Merge your branch into the local ’master’ branch.
### 6. If there are conflicts, we want the paragraph to appear in alphabetical
order in the final README.md file.
### 7. Push your changes in the ’master’ branch to the remote repository.

## Exercise 5

### For the repository owner... In the web UI, add a line of text at the
beginning of the README.md with the team members’ names or aliases.
Using only the shell in your local repository :
### 1. Pull the latest changes in the ’master’ branch, check the README.md
is up-to-date (contains all the paragraphs and the new line).
### 2. Switch back to your own branch (not including the latest changes from
the master branch).
### 3. Merge the changes from ’master’ to your own branch.
### 4. Commit this change

## Exercise 6

### Using only the shell in your local repository :
### 1. Delete your branch on local repository.
### 2. Delete your branch on distant repository

## Exercise 7

### Using only the shell in your local repository :
### 1. Pull the latest changes in the ’master’ branch.
### 2. Create a new local branch named after you and switch to it.
### 3. Then with a separate commit for each change :
### (a) Clear the whole file, removing all text.
### (b) Add a title line "Git interactive rebase".
### (c) Copy the first paragraph from https ://git-scm.com/book/en/v2/Git Tools-Rewriting-History.
### (d) Add the second paragraph from the same page.
### (e) Add the first and second paragraphs from the "Changing Multiple
Commit Messages" section in the same page.
### (f) Remove the second paragraph from your file.
### (g) Add the missing title "Changing Multiple Commit Messages" on a
line just before the two paragraphs your copied (before To modify a
commit that is farther back in your history...).
### (h) Add a final line with your name or alias.
The commit history of your branch should then be a bit messy with 8
commits.
### 4. Use interactive rebase to have a single commit with message "Explain git
interactive rebase.".
### 5. Push your branch on the remote repository.

## Exercise 8

