# Git Setup :sunglasses:

1. Make a github account.
2. Request to join the [CHSR 2024](https://github.com/orgs/Tino-FRC-2473/teams/software-2024) team.
3. Install git following instructions in [the section below](#install-git-bash-desktop).
4. Configure your local git environment by entering these commands in the terminal:

``` 
    Set your name: 
    git config --global user.name <firstname lastname>

    Set your email: 
    git config --global user.email <your email>

    Set VS Code as your default editor for git
    git config --global core.editor "code --wait"

    (optional) Always rebase on branch pulls: 
    git config --global branch.autosetuprebase always
```
> [!NOTE]
> When setting your email make sure you don't set is as your private email adress and instead use the `noreply` email adress provided by github. This email adress in in the form of `ID+USERNAME@users.noreply.github.com`.

## Install git bash! :desktop:

### Windows :window:
- The easiest way to install git is via [this link](https://git-scm.com/download/win).
    - Though binary installers like the ones in the link may be slightly behind, these version differences will likely not make a difference for our purposes.

### Mac :apple:
- Run `git --version` from the terminal; will either return the current version or prompt installs
- If that doesn't work, install git via [this link](https://git-scm.com/download/mac).

### Linux :penguin:
- Follow instructions on [this link](https://git-scm.com/download/linux) for preferred package manager installation of linux


## Install github desktop! :tv:
- The commands provided throughout the exercises in the training will NOT be for github desktop, which is gui based (no commands). While it's more convenient for our purposes, it will be better throughout your coding journeys to understand how to use git bash, as it offers more customizability and support for niche tasks. As you use it more, you will learn it is also significantly faster to use than github desktop.
    - **The practical test will require that you know how to work with git bash, not github desktop.**
    - Despite this, if you want to have github desktop for personal purposes or throughout the season, you can install it via [this link](https://docs.github.com/en/desktop/installing-and-authenticating-to-github-desktop/installing-github-desktop). 