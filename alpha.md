## if you wanna start from scratch project and push that to your github , then you need to
- `git init` to initialize git
- `git commit -a -m "skip staging, commit directly!"` to commit changes in git
- `git remote add origin YOUR_GITHUB_REPOSITORY_URL` to setup url
- `git remote -v` to verify if url is setup correctly
- `git push -u origin main` to push changes

##  You have created repo in github, all initialized via github UI and now you wanna clone it to local machine and push changes locally before updating on github
- `git clone YOUR_GITHUB_REPOSITORY_URL.git`
- __introduce changes__
- EITHER:
  - `git add .` and `git commit -m "_COMMIT_DETAILS_"`
  - `git commit -a -m "__skipStaging_commitDirectly__"`
- `git push origin main`

## HOW TO SETUP UP PERSONAL ACCESS TOKEN 
- when you execute git push you will be prompted to give `username` and `password`
- since github removed support for password you need to give __PAT__ in password section
> MAIN_SETTINGS > DEV SETTING (bottom) > PAT > GENERATE
- make sure to give limited permission, mostly i need only `repo` block to be checked && set short-time expiration

## WHY n HOW TO WORK ON SEPARATE BRANCH
- best convention is to work on separate branch instead of main branch, it gives lot of room to avoid bugs and also offers environment for multiple developers to push changes
independently with no effect on main branch

- __USAGE COMMANDS__
- `git checkout -b _BRANCH_NAME_` creates separate branch to work on
- `git switch _BRANCH_NAME_ / main` to switch between branches
- `git branch` or `git branch -vv` to view which branch you currently are on, later one for more detail
- stage and commit changes inside this branch
> __REMEMBER CHANGES INTRODUCED IN SEPARTE BRANCH WILL NOT APPEAR WHEN YOU SWITCH BRANCHES to main__
- Now, if you wanna merge changes introduced in separate branch
- switch to main branch and run `git merge _BRANCH_NAME` and the changes will be introduced to main repo

## Debugging and Logging
- `git status` to check what git actions to perform
- `git log` to check alltime changes
- `git log -p` to check alltime changes along with actual changes in each commit

## Reverting changes
- `git revert <commit-hash>` to revert back changes introduced by particular commit
> you get commit hash by running __$git log__
- git restore <filename>` to remove changes to a file __I DONT UNDERSTOOD THIS PROPERLY RIGHT NOW AND DONT FEEL NEED__


