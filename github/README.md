
# Two-factor authentication or SAML sign on

Generate a personal token as password.  See instructions for the https (recommended): https://help.github.com/articles/which-remote-url-should-i-use/


```
git clone https://github.com/username/repo.git
Username: your_username
Password: your_token
```



#Pattern

How to test a merge without actually merging into the development branch

```sh
git checkout featureBranch
git pull origin featureBranch
git checkout development
git pull origin development
git checkout -b tempDevMergeBranch
git merge featureBranch
```
Later delete the local branch.
```sh
git branch -d tempDevMergeBranch
```
