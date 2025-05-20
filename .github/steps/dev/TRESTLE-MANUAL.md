## Step 2: Fork the trestle-bot repository 🍴

_This will be your own copy of trestle-bot_

### 📖 Theory: Fork first, clone later. 

<!-- GitHub-styled notifications can be used outside ordered lists. Available options are: NOTE, IMPORTANT, WARNING, TIP, CAUTION -->
<!--
 [!NOTE]
> (Important note or additional information relevant to this section)
 -->

Read the GitHub [Forking a Repository](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) documentation for a better understanding of how to manage your fork. 

### ⌨️ Activity: Cloning the forked trestle-bot repository to your local file system. 
<!--._but... what is a fork? what is cloning?_-->

<img src="https://github.com/user-attachments/assets/cb41a75b-1a12-43cf-a62b-4621f18240ec" alt="Alt Text" width="800" height="600">


#### 🗺️🍴Navigate to the upper right corner of the trestle-bot repository and click _Fork_

- Create your own copy of the trestle-bot repository under your GitHub Username.:octocat:

<img src="https://github.com/user-attachments/assets/38edd6cc-4390-4bca-ad74-8db55517e17a" alt="Alt Text" width="650" height="400">

2. **Set-up your local environment:** on your computer, navigate to the terminal. To ensure a uniform setup, follow the direction below to create a folder on your computer called `CPLYTM`. The `CPLYTM` folder will house the repositories that you want to use locally. 🍴

**Create the folder `CPLYTM`**
|Architecture Compatability  💻    |  Command in Terminal    |       Output                                                           |
|----------------------------------|:-----------------------:|:----------------------------------------------------------------------:|
|🍎arm64 (macOS/Darwin)            |  `mkdir CPLYTM`         | Running `ls` will show the new folder `CPLYTM`                         |
|🐧amd64 (Linux machines)          |  `mkdir CPLYTM`         | Running `ls` will show the new folder `CPLYTM`                         |

**Change directories into the `CPLYTM` folder to start working**
|Architecture Compatability  💻    |  Command in Terminal    |       Output                                                           |
|----------------------------------|:-----------------------:|------------------------------------------------------------------------|
|🍎arm64 (macOS/Darwin)            |  `cd CPLYTM`            | Running `ls` in `CPLYTM` will show the contents of the `CPLYTM` folder |
|🐧amd64 (Linux machines)          |  `cd CPLYTM`            | Running `ls` in `CPLYTM` will show the contents of the `CPLYTM` folder |

3. **Clone the trestle-bot repository:** on your computer, navigate to the terminal. To ensure a uniform setup, create a folder on your computer called CPLYTM.

**Cloning the repository**:octocat:
|Command in `CPLYTM` folder 📂                             |  Result                            |
|----------------------------------------------------------|------------------------------------|
|`git clone https://github.com/{$GITHUB_USERNAME}/trestle-bot.git` |This command will create a copy of [trestle-bot](https://github.com/complytime/trestle-bot#) on your computer         |
|`cd trestle-bot`                                          |This command allows you to change directories and see the contents of the trestle-bot repo                            |

**Setting up the remote upstream**🔄
|Command in `trestle-bot` folder   🤖📂                    |  Result                                                                                                              |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
|`git remote -v`                                           |This command allows you to check the `upstream` branch which will have the most-recent updates of trestle-bot content |
|`git remote add upstream https://github.com/complytime/trestle-bot.git`|This command sets the upstream trestle-bot remote repository for syncing changes to your trestle-bot forked repository|

[_A bit more context on upstream vs. downstream and why it's important_](https://www.redhat.com/en/blog/what-open-source-upstream)
