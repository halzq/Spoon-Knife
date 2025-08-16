# forking
## Understanding connections between repositories(如何知道儲存庫之間關係)
https://docs.github.com/en/repositories/viewing-activity-and-data-for-your-repository/understanding-connections-between-repositories#viewing-a-repositorys-network

## Fork a repository (如何實際操作fork)
https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo?tool=desktop
For example, you can use forks to propose changes related to fixing a bug.
Rather than logging an issue for a bug you have found, you can:

1. Fork the repository.
2. Make the fix.
3. Submit a pull request to the project owner.

### I. Forking a repository (一 fork)
1. On GitHub, navigate to the octocat/Spoon-Knife repository.
在 GitHub 上，前往 octocat/Spoon-Knife 儲存庫。

2. In the top-right corner of the page, click Fork.
在頁面右上角，點擊 Fork。

3. Then this repository would be forked to your own github account.
這樣就會被fork到我的帳號內了

### II. Cloning your forked repository (二 clone)
This step is to have the files in that repository locally on your computer.

1. On GitHub, navigate to your own fork of the Spoon-Knife repository.

2. Above the list of files, click <> Code. Copy the URL for the repository.

3. Open terminal and type
```bash
git clone https://github.com/YOUR-USERNAME/Spoon-Knife
```

4. Press Enter. Your local clone will be created.

### III. sync your fork with the upstream repository (三 remote add)
When you fork a project in order to propose changes to the upstream repository,
you can configure Git to pull changes from the upstream repository into the local clone of your fork.
1. look up the status
```bash
$ git remote -v
> origin  https://github.com/YOUR-USERNAME/YOUR-FORK.git (fetch)
> origin  https://github.com/YOUR-USERNAME/YOUR-FORK.git (push)
```

2. add upsteam or origin to the local repo
```bash
git remote add upstream https://github.com/ORIGINAL-OWNER/Spoon-Knife.git
git remote add origin https://github.com/YOUR-USERNAME/YOUR-FORK.git
```

3. To verify the new upstream repository you have specified for your fork, type git remote -v again.
You should see the URL for your fork as origin, and the URL for the upstream repository as upstream.
```bash
$ git remote -v
> origin    https://github.com/YOUR-USERNAME/YOUR-FORK.git (fetch)
> origin    https://github.com/YOUR-USERNAME/YOUR-FORK.git (push)
> upstream  https://github.com/ORIGINAL-OWNER/ORIGINAL-REPOSITORY.git (fetch)
> upstream  https://github.com/ORIGINAL-OWNER/ORIGINAL-REPOSITORY.git (push)
```