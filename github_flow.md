# Github flow

## We have agreed, that we will work using Github flow. Simple instructions can be found below.

In short words, we are forking repository from Code for Poznan organisation to our repository, push the changes there and create pull requests from our branches (eg. wistler/sample_branch) to codeforpoznan/master. 

## Link for reference: https://guides.github.com/introduction/flow/

Example config for proper Github flow.
"""
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
"""

Example commands:

1. git fetch upstream
  1. To fetch upstream repository (newest changes from master branch from upstream repository - in that case Code for Poznan's main branch for particular project)
1. git merge upstream/master
  1. To merge all the changes from upstream repository to master branch
1. git push
  1. to push all of the changes to forked repository

Flow for own repositories is simple:

1. create your own branch 
  1. git checkout -b name_of_your_branch
1. make changes in the code
1. add the changes
  1. git add name_of_the_file
1. commit the files 
  1. git commit -m "message that explains the commit"
1. push the changes to your own repository
  1. git push origin name_of_your_branch
1. go to Github website and create Pull Request from head eg. wistler/sample_branch to base codeforpoznan/master