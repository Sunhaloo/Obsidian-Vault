---
Alias: NeoVim Tutorial
Tag: nvim, tutorial
Author: S.Sunhaloo
Date: 16-07-2023
---

---

## List Of Contents: 

- [[NeoVim Installation#How to Install NeoVim| NeoVim Installation]]
	- [[NeoVim Installation#Windows Install| Windows]]
	- [[NeoVim Installation#Linux Install| Linux]]
	- [[NeoVim Installation#Mac Install| Mac OS]]
- [[NeoVim Installation#Installing NvChad| Installing NvChad]]
	- [[NeoVim Installation#Installing Git| Installing Git]]
	- [[NeoVim Installation#NvChad Website:| NvChad Installation]]

---

>[!tip] Remember
>These is not ***notes***; but rather **Documentation**

---

# How to Install NeoVim 

## Windows Install

On Windows obviously it will be more *difficult* that on Linux or Mac because of the difference in their terminal and operating system.

Windows uses **PowerShell** and **Command Prompt** or **CMD** while Linux and Mac OS *Bash* which are **different** and the commands are also **different**.
Nevertheless, **Bash** has recently gained traction on *Windows*.

---

>[!info]
>It is recommended to install the new **Terminal** and **PowerShell** from the *Microsoft Store*

### PowerShell

After opening PowerShell, we will need to install **scoop**.

Scoop is a *package manager* used to **install** and **manage** software packages on Windows.

Paste the follow lines of code into PowerShell to install *Scoop*:

```powershell

# Optional: Needed to run a remote script the first time
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser

# Installs scoop
irm get.scoop.sh | iex

```

>[!note]
>Another *package manager* is *Chocolatey*
>But in this case we used *Scoop*

### Installing NeoVim on Windows

```powershell

scoop install neovim

```

>[!note]
>This will install **basic** NeoVm without any *configurations*

## Where are the Files Stored ( For Windows )

The files are stored in the folder "nvim" which is located in:

```powershell

C:\Users\azmaa\AppData\Local\nvim

```

>[!warning]
>Mine is installed on the *"C"* drive
>If your drive is **different**, **copying** the above path will **not** work

---

## Linux Install

On Linux, it is really **easy**!

We just need to open the *terminal* and type the following commands:

```bash

sudo apt install neovim

```

>[!note]
>Again;
>This will install **basic** NeoVim without any *configurations*

---

## Mac Install

First of all, we need to install **Homebrew**; it is similar to*Scoop* on *Windows*.
It is a *package manager* for Mac operating system

```bash

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

```

### Installing NeoVim On Mac OS

```bash

brew install neovim

```

>Again,
>This will install **basic** neovim without any *configurations*

---

# Installing NvChad 

NvChad is a *NeoVim* configuration written in **Lua** aiming to provide a base configuration with very beautiful UI and fast startup time.

## Installing Git

You will need to install **Git** to clone into the repository

### Windows Install

Copy the following code below to install *git*:

```powershell

scoop install git

```

### Linux Install

Copy the following code below to install *git*:

```bash

sudo apt install git

```

### Mac OS

Copy the following code below to install *git*:

```bash

brew install git

```

---

## NvChad Website:

To read more about NvChad, head over to:

**Website:** [NvChad](https://nvchad.com/docs/quickstart/install)

There you will find the tutorial to install NvChad and other documentation about the program!

----

>[!note]
>For **Linux** and **Mac OS**
>I do not know where are the files specifically stored
>For **Linux**: it should be stored in the *home* directory and
