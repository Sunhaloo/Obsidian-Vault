---
alias: Neovim
tag: nvim
date: 16-07-2023
---

---

## List Of Contents: 

- [[Neovim#How to Install Neovim| Neovim Installation]]
	- [[Neovim#On Windows:| Windows]]
	- [[Neovim#On Linux:| Linux]]
	- [[Neovim#On Mac OS| Mac OS]]
- [[Neovim#Installing NvChad | Installing NvChad]]
	- [[Neovim#Installing Git | Installing Git]]
	- [[Neovim#NvChad Website:| NvChad Installation]]

---

# How to Install Neovim 

## On Windows:

On Windows obviously it will be more *difficult* that on Linux or Mac because of the difference in their terminal.
Windows uses **Powershell** and **Command Prompt** while Linux and Mac OS *terminal* are quite similar to each other.

>[!info]
>It is recommended to install the new **Terminal** and **Powershell** from the *Microsoft Store*

### Powershell

After opening Powershell, we will need to install **scoop**.

Scoop is a *package manager* used to **install** and **manage** software *packages* on Windows.

Paste the follow lines of code into Powershell:

```powershell

Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
# Optional: Needed to run a remote script the first time

irm get.scoop.sh | iex

```

>[!note]
>Another *package manager* is **chocolatey**
>But in this case we used *scoop*

### Installing Neovim on Windows

```powershell

scoop install neovim

```

>[!note]
>This will install **basic** neovim without any *configurations*

## Where are the Files Stored

The files are stored in the folder nvim which is located in:

```powershell

C:\Users\azmaa\AppData\Local\nvim

```

>[!warning]
>Mine is installed on the *"C"* drive
>If your drive is **different**, **copying** the above path will **not** work

## On Linux:

On Linux, it is really **easy**!

We just need to open the *terminal* and type the following commands:

```bash

sudo apt install neovim

```

>[!note]
>Again,
>This will install **basic** neovim without any *configurations*

## On Mac OS

First of all, we need to install **Homebrew**; it is similar *scoop* on *Windows*. It is a *package manager* for Mac operating system

```bash

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

```

### Installing Neovim On Mac OS

```bash

brew install neovim

```

>Again,
>This will install **basic** neovim without any *configurations*

---

# Installing NvChad 

NvChad is a *neovim* configuration written in **lua** aiming to provide a base configuration with very beautiful UI and fast startup time

## Installing Git

You will need to install **Git** to clone into the repository

### On Windows

Copy the following code below to install *git*:

```powershell

scoop install git

```

### On Linux

Copy the following code below to install *git*:

```bash

sudo apt install git

```

### On Mac OS

Copy the following code below to install *git*:

```bash

brew install git

```

---

## NvChad Website:

To install NvChad, head over to:

**Website:** [NvChad](https://nvchad.com/docs/quickstart/install)

There you will find the tutorial to install NvChad.

----

>[!note]
>For **Linux** and **Mac OS**
>I do not know where are the files stored
>For **Linux**: it should be stored in the *home* directory and

---

S.Sunhaloo