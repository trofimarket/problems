# TroFi Problem Tracker

All problems added to the issue tracker SHOULD follow the C4 Protocol.

## Contributing to TroFi    
The contribution policy we follow is the [Collective Code Construction Contract (C4)](/CONTRIBUTING.MD)    

If you're wondering why any of the rules in the C4 are there, take a look at the [line by line explanation](/DESCRIPTIVE_C4.MD) of everything in the C4, this explains the rationale and history behind everything in the protocol and makes it easier to understand.


<details>
  <summary>Step-by-step guide to sending a pull request</summary>
<p>
  
  
**It is important to claim the issue you want to work on so that others don't work on the same thing. Make a comment in the issue: `I'm claiming this issue to work on it` before you start working on the issue. Or if you're an existing Contributor and can assign yourself to the issue, do that instead.**

If at some point you want to abandon the issue and let someone else have a go, let everyone know by unassigning yourself and/or commenting appropriately. If you claim an issue and do not send a pull request within 24 hours a Maintainer MAY remove you from the issue and let someone else claim it.

0. Read the [contribution protocol](/CONTRIBUTING.MD) and the [line by line explanation](/DESCRIPTIVE_C4.MD) of the protocol.
1. Fork this github repository under your own github account.
2. Clone _your_ fork locally on your development machine.
3. Choose _one_ problem to solve. If you aren't solving a problem that's already in the issue tracker you should describe the problem there (and your idea of the solution) first to see if anyone else has something to say about it (maybe someone is already working on a solution, or maybe you're doing somthing wrong).
4. Add the repository you are working on as an upstream source and pull any changes:
```
@: git remote add upstream git://github.com/trofimarket/contracts //only needs to be done once
@: git checkout master //just to make sure you're on the correct branch
@: git pull upstream master //this grabs any code that has changed, you want to be working on the latest HEAD
@: git push //update your remote fork with the changes you just pulled from upstream master
```
5. Create a local branch on your machine `git checkout -b branch_name` (it's usually a good idea to call the branch something that describes the problem you are solving). _Never_ develop on the `master` branch, as the `master` branch is exclusively used to accept incoming changes from `upstream:master` and you'll run into problems if you try to use it for anything else.
6. Solve the problem in the absolute most simple and fastest possible way with the smallest number of changes humanly possible. Tell other people what you're doing by putting _very clear and descriptive comments in your code every 2-3 lines_.    
Add your name to the AUTHORS file so that you become a part owner of the codebase.    
7. Commit your changes to your own fork:
Before you commit changes, you should check if you are working on the latest version (again). Go to the github website and open _your_ fork of the repository, it should say _This branch is even with xxxxxxxx:master._    
If **not**, you need to pull the latest changes from the upstream repository and replay your changes on top of the latest version:
```
@: git stash //save your work locally
@: git checkout master
@: git pull upstream master
@: git push
@: git checkout -b local_branch_name //from step 5
@: git stash pop //_replay_ your work on the new branch which is now fully up to date with the Blockrazor repository
```

Note: after running `git stash pop` you should run any tests, check that everything compiles properly, etc, and look over your code again and check that everything still works as sometimes a file you worked on was changed in the meantime, breaking one of your changes.

Now you can add your changes:   
```
@: git add changed_file.sol //repeat for each file you changed
```

And then commit your changes:
```
@: git commit -m 'problem: <50 characters describing the problem //do _not_ close the '', press ENTER two (2) times
>
>solution: short description of how you solved the problem.' //Now you can close the ''. Be sure to mention the issue number if there is one (e.g. #6)    
@: git push //this will send your changes to _your_ fork on Github
```    
8. Go to your fork on Github and select the branch you just worked on. Click "pull request" to send a pull request back to the upstream repository.
9. Send the pull request, be sure to mention the issue number with a # symbol at the front (e.g. #11).  
10. Go back to the issue, and make a comment:
  ```
    Fixed in #(PR_NUMBER)
  ```
  
  This will label this issue as complete, and everyone can test your solution and close the issue if it solves the problem.

#### What happens after I send a pull request?    
If your pull request contains a correct patch (read the C4) a maintainer will merge it.
If you want to work on another problem while you are waiting for it to merge simply repeat the above steps starting at:
```
@: git checkout master
```
