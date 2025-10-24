# stash_practice

task given: Git Stash Scenario
•	Create a repo stash_practice.
•	Modify two files and don’t commit them.
•	Run git stash to temporarily save your work.
•	Switch to a new branch bugfix and make a new commit.
•	Return to main and apply your stash using git stash apply.
•	Push final code and share output of git stash list.

steps to be followed:
1. create a new repo in the remote cloud and then clone the repo to the server
  --> git clone <url>
2. Create and commit initial files
 --> echo "Initial content in file1" > f1.txt
 --> echo "Initial content in file2" > f2.txt
 --> git add .
 --> git commit -m "Initial commit with two files"
3. Modify two files but don’t commit
 --> echo "New changes in file1" >> f1.txt
 --> echo "New changes in file2" >> f2.txt
 --> Check uncommitted changes: git status
4. Stash the changes
 --> git stash 
 --> to see the stashed list : git stash list
5. Create new branch and make a new commit
 --> git checkout -b bugfix
 --> echo "Bug fixed here" > bugfix.txt
 --> git add bugfix.txt
 --> git commit -m "Added bugfix file"
6.Switch back to main and apply the stash
 --> git checkout main
 --> git stash apply
7.Commit and push the final code
 --> git add .
 --> git commit -m "Applied stashed changes on main branch"
 --> git push -u origin main
 --> git push origin bugfix
8. Verify stash list: git stash list
9. drop the stash : git stash grop


