# Github flow

## We have agreed, that we will work using Github flow. Simple instructions can be found below.

In short words, we are forking repository from Code for Poznan organisation to our repository, push the changes there and create pull requests from our branches (eg. ``w1stler:sample_branch``) to ``codeforpoznan:master``. 

## Link for reference: https://guides.github.com/introduction/flow/

How to setup your local repository?

1. Fork repository from Code for Poznań
2. Clone your (forked) repository to local computer
3. Add upstream remote by executing command ``git remote add upstream git@github.com:CodeForPoznan/project_name.git``

Example config for proper Github flow after changes.

```
[core]
        repositoryformatversion = 0
        filemode = true
        bare = false
        logallrefupdates = true
[remote "origin"]
        url = git@github.com:w1stler/project_name.git
        fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
        remote = origin
        merge = refs/heads/master
[remote "upstream"]
        url = git@github.com:CodeForPoznan/project_name.git
        fetch = +refs/heads/*:refs/remotes/upstream/*
```

How to be up-to-date with upstream repository?

1. `git fetch upstream`
  * To fetch upstream repository (newest changes from master branch from upstream repository - in that case Code for Poznan's main branch for particular project)
2. `git merge upstream/master`
  * To merge all the changes from upstream repository to master branch
3. `git push`
  * to push all of the changes to forked repository

How to propose change in upstream repository?

1. create your own branch 
  * `git checkout -b name_of_your_branch`
2. make changes in the code
3. add the changes
  * `git add name_of_the_file`
4. commit the files 
  * `git commit -m "message that explains the commit"`
5. push the changes to your own repository
  * `git push origin name_of_your_branch`
6. go to Github website and create Pull Request from head eg. w1stler:sample_branch to base codeforpoznan:master