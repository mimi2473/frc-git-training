# git setup :sunglasses:

1. make a github account.
2. request to join the [CHSR 2024](https://github.com/orgs/Tino-FRC-2473/teams/software-2024) team.
3. install git following instructions in [the section below](#install-git-bash-desktop).
4. configure your local git environment by entering these commands in the terminal:

``` 
    Set your name: 
    git config --global user.name <firstname lastname>

    Set your email 💞: 
    git config --global user.email <your email>

    (optional) Always rebase on branch pulls: 
    git config --global branch.autosetuprebase always

    (optional) Set VS Code as your default editor for git
    git config --global core.editor "code --wait"
```

## install git bash! :desktop:

### windows :window:
- the easiest way to install git is via [this link](https://git-scm.com/download/win).
    - though binary installers like the ones in the link may be slightly behind, these version differences will likely not make a difference for our purposes.

### mac :apple:
- run `git --version` from the terminal; will either return the current version or prompt installs
- if that doesn't work, install git via [this link](https://git-scm.com/download/mac).

### linux :penguin:
- follow instructions on [this link](https://git-scm.com/download/linux) for preferred package manager installation of linux


## install github desktop! :tv:
- the commands provided throughout the exercises in the training will NOT be for github desktop, which is gui based (no commands). while it's more convenient for our purposes, it will be better throughout your coding journeys to understand how to use git bash, as it offers more customizability and support for niche tasks. as you use it more, you will learn it is also significantly faster to use than github desktop.
    - **the practical test will require that you know how to work with git bash, not github desktop.**
    - despite this, if you want to have github desktop for personal purposes or throughout the season, you can install it via [this link](https://docs.github.com/en/desktop/installing-and-authenticating-to-github-desktop/installing-github-desktop). 