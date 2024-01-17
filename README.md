# Guidance

Welcome to the [AI for Net Zero](https://www.imperial.ac.uk/ai-net-zero/#:~:text=In%20order%20to%20optimise%20UK,and%20the%20latest%20computing%20hardware.) GitHub Team page!  This is a permanent home for our codebase, documentation of experiments, packages, apps and more.  

In this document you'll find guidance about how to join the team, add repos, etc., as well as links to more general information on topics such as version control with git.

This is an evolving document, so come back every once in a while. If you have any suggestions for additional content then please [raise an issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue)!

## Joining the team
If you have an active *imperial.ac.uk* email address you can join the AI for Net Zero GitHub Team by

1. If you do not already have one, creating a GitHub account linked to your *imperial.ac.uk* email address. GitHub allows you to have multiple personal accounts as long as they are linked to different email addresses
2. Then [follow the steps here](https://www.imperial.ac.uk/admin-services/ict/self-service/research-support/research-support-systems/github/working-with-githubcom/) to **link your Imperial GitHub account to the Imperial College GitHub.com organisation**.
3. Once you've been admitted, send your GitHub user name to one of the [team admins](https://github.com/RSE-AI-for-Net-Zero/AI_for_NZ_guidance/blob/main/README.md#current-team-admins), who will add you to the team.

If you do not have an active *imperial.ac.uk* email address then you can still participate on a per-repo basis as an [outside collaborator](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/managing-teams-and-people-with-access-to-your-repository#inviting-a-team-or-person) - contact either the repo owner or one of the [team admins](https://github.com/RSE-AI-for-Net-Zero/AI_for_NZ_guidance/blob/main/README.md#current-team-admins).


## Adding repos
### Repo visibility

Repositories ("repos") owned by the team can be 
+ *private* - visible only to you,
+ *internal* - visible to Imperial College members and [outside collaborators](https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/managing-outside-collaborators/adding-outside-collaborators-to-repositories-in-your-organization) only or
+ *public* - visible to whole world!

### Creating a repo from scratch
1. Make sure you are logged into your Imperial GitHub account
2. Follow the guidance [here](https://docs.github.com/en/repositories/creating-and-managing-repositories/quickstart-for-repositories) to create a new repo.  In the **owner** drop-down menu (see image below), select *ImperialCollegeLondon*

![screenshot of create repo page](/images/create_repo.png)

3. Now navigate to the [AI for Net Zero repo page](https://github.com/orgs/ImperialCollegeLondon/teams/ai-for-net-zero/repositories) and click the **Add repository** button, search for your newly created repo by name and click **Add repository to team**.

Alternatively, or if you **do not have an Imperial account**, existing publicly visible repos can be forked into the AI for Net Zero team.  Those without Imperial email addresses can then be added as [outside collaborators](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/managing-teams-and-people-with-access-to-your-repository#inviting-a-team-or-person) and given, e.g., read, write or admin permissions for that repo only.  Here are the steps
1. First ensure your repo is publicly visible and then share a link with one of the [team admins](https://github.com/RSE-AI-for-Net-Zero/AI_for_NZ_guidance/blob/main/README.md#current-team-admins)
2. A **team admin** will fork (i.e., create a copy of) your repo under *ImperialCollegeLondon* and then add it to the AI for Net Zero team
3. The team admin will then invite you to be an outside collaborator.


## Further guidance
### Using SSH to authenticate to multiple GitHub accounts from a single machine

1. [Generate public/private key pairs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) for each of your GitHub accounts, giving identifiable file names, e.g., `id_ed25519_imperial` and `id_ed25519_personal` for your Imperial and personal accounts, respectively

2. Tell your SSH Agent while key pair to use to authenticate to which account. Edit, or create if it doesn't already exist, the file `~/.ssh/confg` and add the following

```
# Default github account: AI for Net Zero
Host github-imperial
   HostName github.com
   IdentityFile ~/.ssh/id_ed25519_imperial
   IdentitiesOnly yes
   
# Other github account: personal
Host github-personal
   HostName github.com
   IdentityFile ~/.ssh/id_ed25519_personal
   IdentitiesOnly yes
```
3. When adding a new remote to a local repo, use the annoted Host, rather than github.com in the remote url, e.g.,

```
$ git remote add new_imperial_remote git@github-imperial:my_repo_name.git
```
or
```
$ git remote add new_personal_remote git@github-personal:my_repo_name.git
```
4.  You can amend the url for an existing remote by

```
$ git remote set-url origin git@github-imperial:my_repo_name.git
```



## Resources
### git

Chapters 1 - 5 of [Pro Git](https://git-scm.com/book/en/v2) contain almost everything you need for day-to-day use and is an excellent place to start.  Later chapters go into distributed workflows and git internals

[Version Control with Git](https://www.oreilly.com/library/view/version-control-with/9781492091189/), *Ponuthorai, P. K. and Loeliger, J.*, 3rd Edition, O'Reilly Media, Inc. is great.



## Current team admins
lee.benson@imperial.ac.uk



