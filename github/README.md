#Pattern

How to test a merge without actually merging into the development branch

git checkout featureBranch
git pull origin featureBranch
git checkout development
git pull origin development
git checkout -b tempDevMergeBranch
git merge featureBranch

Later delete the local branch.
git branch -d tempDevMergeBranch
