
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

### For the repository owner... In the web UI, make sure lines 2 to 6 of the README.md are not empty. One person at a time, using only the shell :
### 1. Switch back to your own branch (not including the latest changes from the master branch).
```
git checkout 'name of branch'
```
### 2. Edit the lines 2 to 6 of the README.md file with a text you like (a poem, a quote, some clever code...). It can be any readable text, it may be incomplete, it must just take about 5 lines and be different from your teammates. It must start on line 2 to trigger conflicts between team members.
```
vim README.md
```
### 3. Commit this change.
```
git commit -am "change readme file"
```
### 4. Pull latest status from the remote repository ’master’ branch into your local ’master’ branch.
```
git pull
```
### 5. Merge your branch into the local ’master’ branch.
```
git checkout 'name of branch'
git merge main
```
### 6. If there are conflicts, we want the paragraph to appear in alphabetical order in the final README.md file.
```
git status
vim README.md
```
delete lines and errors and write :wq
```
git commit -am "solve conflicts"
```
### 7. Push your changes in the ’master’ branch to the remote repository.
```
git push
```
## Exercise 5

### For the repository owner... In the web UI, add a line of text at the beginning of the README.md with the team members’ names or aliases. Using only the shell in your local repository :
### 1. Pull the latest changes in the ’master’ branch, check the README.md is up-to-date (contains all the paragraphs and the new line).
```
git pull
cat README.md
```
### 2. Switch back to your own branch (not including the latest changes from the master branch).
```
git checkout 'name of branch'
```
### 3. Merge the changes from ’master’ to your own branch.
```
git merge main
```
### 4. Commit this change
```
git commit
git push origin 'name of branch'
```

## Exercise 6

### Using only the shell in your local repository :
### 1. Delete your branch on local repository.
```
git checkout main
git branch -d 'name of branch'
```
### 2. Delete your branch on distant repository
```
git push origin --delete 'name of branch'
```

## Exercise 7

### Using only the shell in your local repository :
### 1. Pull the latest changes in the ’master’ branch.
```
git checkout master
git pull
```
### 2. Create a new local branch named after you and switch to it.
```
git checkout -b your_name_branch
```
### 3. Then with a separate commit for each change :
### (a) Clear the whole file, removing all text.
```
echo "" > README.md
git add README.md
git commit -m "Clear README.md"
```
### (b) Add a title line "Git interactive rebase".
```
echo "# Git interactive rebase" > README.md
git add README.md
git commit -m "Add title"
```
### (c) Copy the first paragraph from https ://git-scm.com/book/en/v2/Git Tools-Rewriting-History.
```
echo "One of the most common..." >> README.md
git add README.md
git commit -m "Add first paragraph"
```
### (d) Add the second paragraph from the same page.
```
echo "However, you can also..." >> README.md
git add README.md
git commit -m "Add second paragraph"
```
### (e) Add the first and second paragraphs from the "Changing Multiple Commit Messages" section in the same page.
```
echo "To modify a commit..." >> README.md
echo "" >> README.md
echo "If you want to..." >> README.md
git add README.md
git commit -m "Add paragraphs from Changing Multiple Commit Messages section"
```
### (f) Remove the second paragraph from your file.
```
sed -i '/However, you can also/d' README.md
git add README.md
git commit -m "Remove second paragraph"
```
### (g) Add the missing title "Changing Multiple Commit Messages" on a line just before the two paragraphs your copied (before To modify a commit that is farther back in your history...).
```
sed -i '/To modify a commit/a ## Changing Multiple Commit Messages' README.md
git add README.md
git commit -m "Add section title"
```
### (h) Add a final line with your name or alias. The commit history of your branch should then be a bit messy with 8 commits.
```
echo "- Your Name or Alias" >> README.md
git add README.md
git commit -m "Add name or alias"
```
### 4. Use interactive rebase to have a single commit with message "Explain git interactive rebase.".
```
git rebase -i HEAD~8
```
### 5. Push your branch on the remote repository.
```
git push origin your_name_branch
```
