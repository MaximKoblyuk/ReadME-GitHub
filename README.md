![image](https://user-images.githubusercontent.com/89156031/223420434-d3c5bce5-d366-4b02-9785-c263f83ec8be.png)



First clone repo  by command: 


git clone https://github.com/.....

2. Create new feature branch from main branch with command:


git branch feature/<task_name>

3. Then checkout to your branch with command: 


git checkout feature/<task_name>

4. Make the changes

5. Add and push the changes with command: 


git add .
git commit -m "task_name"
git push feature/<task_name>
6. Go to Github repository and create Pull Request into main branch and then just wait when the PR is approved by admin of the repository.


Git Merge
 

We have the fix ready, so let's merge the master and fix or branches with features.

git checkout master 

Switched to branch 'master'

Now we merge the current branch (master) with emergency-fix:

Example

git merge emergency-fix
Updating 09f4acd..dfa79db
Fast-forward
 index.html | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
And don’t forget the push our fix code in Azure

git push

Since the emergency-fix branch came directly from master, and no other changes had been made to master while we were working, Git sees this as a continuation of master. So it can "Fast-forward", just pointing both master and emergency-fix to the same commit.

As master and emergency-fix are essentially the same now, we can delete emergency-fix, as it is no longer needed:

git branch -d emergency-fix 

Deleted branch emergency-fix (was dfa79db).
