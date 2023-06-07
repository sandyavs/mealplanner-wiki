# The Standard Development Flow

The branch management strategy for CivicTech will borrow heavily from the '[GitHub Flow](https://guides.github.com/introduction/flow/)' branch-based workflow.  Contributors should know and understand the GitHub Flow. As in GitHub Flow, the 'master' branch for any project should only ever contain fully tested and releasable code. In addition to master we also have a shared development branch (often called 'develop' but may have other names like 'release_dev'). The objective with this shared development branch is that it will be the common place where individual feature branches merge in preparation for a release. Only completed features should be merged into the development branch. At all times the code in the development branch should be testable by the team. Before merging new feature code into the development branch, it should be tested in the feature branch. Feature branches should always be up to date with development to be sure that new features will work once merged into development.

For mealplanner, we have extended the flow to add an extra stage. All feature work will be based off the `v2` branch. Individual features or bugs will be branched from `v2` according to guidelines below and merged into `v2` on completion for integration testing. Periodically, `v2` will be mereged into `develop` and release testing will be performed there. Also any demos or playbacks will be based on `develop`.

When starting work on a new feature or story, create a new branch off of `v2` and give it a meaningful name that relates to the feature. These are referred to as 'feature' branches. As you develop and commit changes to the feature be sure to create descriptive and helpful commit messages. This helps reviewers and testers understand the incoming changes. Once a feature is complete and merged into development, the feature branch can be removed. This will keep the repository from being cluttered with a zillion no longer used branches. All pull requests should have an associated Issue.

Our Flow will therefore will have an extra branch compared with the normal GitHub Flow.

[[gitflow.png]]

Members of the Civic Tech Fredericton organization and teams will contribute to projects using the Shared Repository model. In this project model all branching and pull requests are made in the original repository.  Contributors from outside the CivicTechFredericton organization will use the Fork+Pull project model. In the Fork + Pull model developers will create a fork of our repository and manage their own development process. Once they have completed feature development they can open a pull request with the original repository and a Civic Tech Fredericton member can review and merge it.

# Protected Branches and Permissions

Protected branches in github have additional constraints on merging pull requests. By protecting a branch an administrator can enforce certain checks and balances. In Civic Tech Fredericton projects the `develop` and `v2` branches will be protected. Pull requests will require a review before being merged.  There are no restrictions on feature branches.

Pull requests in github offer the opportunity to create discussions about the request, the changes in it and even to comment directly on specific lines of code. A reviewer of a pull request should use these features to be sure they understand the changes or to raise concerns. 

Release candidates should be prepared and tested completely in the development branch and only when it is ready for release will a pull request be opened for master.  During the phase of preparing for release, pull requests to the development branch should be restricted to only bug fixes so that no new untested code is introduced.

# GitHub Administration

There should always be three organization administrators for Civic Tech Fredericton and two repository admins for each repository. Repository admins should be project leaders or senior developers that can take responsibility for merges and releases.

Respository access can be managed through team membership.  By creating a team per project it is easy to manage access simply by managing teams. 

# Developer guidance

![](https://imgs.xkcd.com/comics/git_2x.png)

## Issues (bugs, features, etc)

Github Issues are the primary building block for project management in mealplanner. Any work done on the code repository, wiki, documentation and any feature requests need to be managed via Issues. There will always be a lot of work to do and therefore a lot of open Issues but the team will decide as a group which are current priorities. Team members should work on and complete Issues assigned to them during the weekly backlog grooming before taking on any additional work. The team uses Zenhub for managing the status and assignment of Issues and the specifics will be reviewed in each meeting.

Issues can be created in a couple of ways: via the Github Issues page or in Github Projects, please use the Github issues page for all Issue creation to ensure correct template usage.

## Branch Naming Conventions

Since dozens of short-lived branches tend to accumulate due to unfinished experiments and so on, please use helpful branch names. It is helpful to start with the issue number followed by a short name for the feature. You can do this automatically from the issue details page by clicking the "Create a branch" link on the right sidebar. This makes it easier to identify when stale branches contain useful but unfinished work.  Every few months stale branches will be removed.

Example

`123-podman-compatibility`

## Commits

With regards to commit messages please make good use of them:
 
1. Make sure to reference the issue # in the message
1. Use the body to explain what and why instead of how

We won't stop you from committing without a proper message but it is just good practice and good manners.

## Other Rules & Important Info:

Master is generally off-limits. If you need to access it you must ask an organisation or repository admin, they are the only ones who can grant access to that branch.

Pull requests to the develop branch must include the list of issues fixed. Also, PRs without test cases should not be accepted. Test cases can be automated via Jest or documented on the [test cases page](Test-cases-v2).

We require public-private ssh keys. If you do not know how to create one see the tutorial [Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent). 
If you do not feel comfortable using the terminal you can use the following, which have been tested and verified to work:
* Git Extensions
* Git within Jet Brains Web Storm IDE
* Git within Jet Brains PyCharm IDE (Full and Community editions)
* Git within VSCode

There are also some GUI git clients like Git Desktop that may be useful.      

You are responsible for deleting your remote branches that are not deleted as part of a pull request. However, there will also be ocasional sweeps to remove stale branches (those that have been unused/unmodified for at least 6 months).

# Resources


Pro Git by Scott Chacon and Ben Straub 
https://git-scm.com/book/en/v2 


Visualizing Git Concepts with D3
http://onlywei.github.io/explain-git-with-d3/ 


Buckey's tutorial on git
https://www.youtube.com/playlist?list=PL6gx4Cwl9DGAKWClAD_iKpNC0bGHxGhcx 

Learn Git Branching
https://learngitbranching.js.org/ 

Git Tricks
https://devhints.io/git-tricks 

Git notes for professionals
https://books.goalkicker.com/GitBook/ 

Learn Git with Git Kraken
https://www.gitkraken.com/learn-git 

***
