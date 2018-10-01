# exploreRebase

This repo is just an experiment on new branchinng scheme, which relies heavily on git rebase to support cI/CD

Here are main branches

1. Master - Always contains the running code. Almost always(always when all test cases are automated) in sync with production.
2. dev - when multiple devoplepors workingn on one codebbase, they merge to dev. Dev get automatically deployed on a platform from 
where developers can perform manual integration testing.

3. issue branch : The bbranch name is the issue number. if multiple repos are affected every branch will have same branch name.
The issue branch is cut from latest master (or latest producton deployment tag). and is always merged to latest master.

If multiple people working and merging to master on same codebase, the debveloper needs to rebase
