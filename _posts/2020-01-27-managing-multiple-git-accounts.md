---
layout: post
title: Managing Multiple Git Accounts
date: 2020-01-27 10:30
summary: Working with multiple git accounts
categories:
---

Lot of companies requests developers to create dedicated `git` accounts to access work related git projects. It is good from security and access control perspective but it is a pain from developers who wish to work on personal projects in their private accounts. Lot of times commits goes in the name of work accounts or the otherway. I have also gone through this that is why have setup my work laptop as below such that there is clear segregation of usage of git accounts

### Prerequisite
   * You should be using ssh based git access which most of the devs would be using. I still find still few are using http based and giving creds each time :man_facepalming:
   * You should be used to segregate your office work space (code folders) from your private workspace  

### Folder Structure

I usually go with the below folder structures. This has helped me in maintaining a clean structure and managing multiple git accounts
```
├── personal
│   └── workspace
│       ├── repo1
│       └── repo2
└── work
    └── workspace
        ├── workrepo1
        └── workrepo2
```

### SSH Keys 
Ensure you create two different `ssh` keys for each of your git accounts. Please refer this [link](https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#adding-your-ssh-key-to-the-ssh-agent).
Once you have the keys ensure to follow this ensure to configure the corresponding `Github` account with corresponding keys. Follow this [link](https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account).
Since you have generated two keys two private key files would be present.

#### SSH Configuration
Since we have two different ssh keys we need to configure it to use it. Below are the ssh configs
```
Host github.com
   HostName github.com
   User git
   IdentityFile ~/.ssh/<private key filename of private account>
   
Host <githubwork.com>    
   HostName github.com
   User git
   IdentityFile ~/.ssh/<private key filename of work account>
```

### Git Configuration
Here I will be setting the default `git config` as my private account and configure work `git` account specific to work associated directories. But we can do the other way based on how we are structuring our workspace.
Below is configuration in default `git config` in `/.gitconfig` 
```
[user]
    name = Personal Git Account Name
    email = personalemailassociatedwithpersonalgit@somedomain
```
The above will ensure all the git operations uses the above config across your machine.

#### Work Related Git Configuration
In the same `~/.gitconfig` add these lines. 
```
[includeIf "gitdir:~/work/"]
    path = ~/work/.gitconfig
```
What we have done is used the `includeif`.[Conditional Includes](https://git-scm.com/docs/git-config#_conditional_includes) was introduced from git 2.13. Ensure you have this version of `git` to use this feature. It actually includes `gitconfig` dynamically based on the conditions. In this case if the git working directory is `~/work` it uses the `.gitconfig` from the `~/work/.gitconfig`.
Below are the contents of this config file inside `~/work/.gitconfig`
```
[user]
    name = Work Git Account Name
    email = workacountemail@domain
```

### How to Work on repositories from Both Account
* To clone a repo from work account you need to follow this since you have configured the `ssh` - `git clone git@githubwork.com:<repopath>.git`
* To clone a repo from private account you need to follow this since you have configured the `ssh` - `git clone git@github.com:<repopath>.git`

All the `git` operations on corresponding repos ensure to follow the corresponding configs. You can customize more configurations in this custom git configs. 

