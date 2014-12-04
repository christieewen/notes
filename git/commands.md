Git/Github Commands Reference
=============================
Steps for merging a new feature branch into develop then master branch.  Checkout, pull, merge, commit, push. Repeat.

* git clone http://github.com/yourRepo.git
* cd yourLocalRepoDir/
* git branch
* git status
* git checkout -b develop
* git pull origin develop
* git merge master
* git commit -a -m "tested and everything is working and there are no conflicts with master and develop so we can continue. yay!"
* git push origin develop
* git checkout -b yourFeature
* git commit -m "made changes and I am ready to merge into develop then master"
* git push origin yourFeature
* git checkout develop
* git merge yourFeature
* git push origin develop
* git checkout master
* git merge develop
* git commit -m "I am currently in master branch and I just merged develop into master then afterwards I will work on a new feature branch"
* git push origin master
* git checkout develop
* git pull origin develop
* git checkout -b newFeature
