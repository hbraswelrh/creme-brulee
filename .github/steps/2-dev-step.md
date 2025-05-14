## Step 2: Initialize the trestle workspace with trestle-bot

_This will house the authored OSCAL content_

### 📖 Theory: Author OSCAL Content and Update it in your [trestle-workspace](https://github.com/hbraswelrh/trestle-workspace/tree/main)

<!--_the one-stop shop for housing your catalogs, profiles, and component-definitions_ -->

<!-- GitHub-styled notifications can be used outside ordered lists. Available options are: NOTE, IMPORTANT, WARNING, TIP, CAUTION -->
<!--
 [!NOTE]
> (Important note or additional information relevant to this section)
 -->

(replace-me: Optional theory or background information relevant to this step)

### ⌨️ Activity: Cloning the trestle-bot repository to your local file system. 
<!--._.but.. what is cloning?_-->

1. **Create an empty GitHub Repository:** the directions to create an empty GitHub repository are [here](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository).
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
|`git clone https://github.com/complytime/trestle-bot.git` |This command will create a copy of [trestle-bot](https://github.com/complytime/trestle-bot#) on your computer         |
|`cd trestle-bot`                                          |This command allows you to change directories and see the contents of the trestle-bot repo                            |

**Setting up the remote upstream**🔄
|Command in `trestle-bot` folder   🤖📂                    |  Result                                                                                                              |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
|`git remote -v`                                           |This command allows you to check the `upstream` branch which will have the most-recent updates of trestle-bot content |
|`git remote add upstream https://github.com/complytime/trestle-bot.git`|This command sets the upstream trestle-bot remote repository for syncing changes to your trestle-bot forked repository|

[_A bit more context on upstream vs. downstream and why it's important_](https://www.redhat.com/en/blog/what-open-source-upstream)

4. **Installing dependencies:dependabot::** The installation of dependencies is cruical for a repository to work properly on your machine. WIP
5. **Creating your own branch 🌴:** Create a branch in the `trestle-bot` repository to work on a documentation fix.

<!-- **Forking the trestle-bot repository:** 🍴
![image](https://github.com/user-attachments/assets/cb41a75b-1a12-43cf-a62b-4621f18240ec)

🗺️🍴**Navigate to the upper right corner of the trestle-bot repository and click _Fork_** 
![image](https://github.com/user-attachments/assets/1f79b331-bfea-411c-a795-b9398ceb063f)

:octocat:Create your own copy of the trestle-bot repository under your GitHub Username. 
![image](https://github.com/user-attachments/assets/38edd6cc-4390-4bca-ad74-8db55517e17a) -->

<!-- IDEEA: CREATE A REPO W A BUNCH OF ERRORS ON DOCS AND THEN GET PRS IN THAT REPO TO HAVE AN AUTOMATED WORKFLOW FOR CONTIBUTIONS!!!!! -->

1. (replace-me: Additional instructions as needed)

<details>
<summary>Having trouble? 🤷</summary><br/>

- Reference the trestle-bot `README.md`.
- (replace-me: Additional troubleshooting tips as needed)

</details>
