---
alias: Vim Usage
tag: nvim
date: 16-07-2023
---

---

## List Of Contents:

- [[How To Use Vim or Neovim#Opening Neovim/NvChad | Opening Neovim/NvChad]]
	- [[How To Use Vim or Neovim#On Windows | Windows]]
	- [[How To Use Vim or Neovim#On Linux | Linux]]
	- [[How To Use Vim or Neovim#On Mac OS | Mac OS]]
- [[How To Use Vim or Neovim#How to Close Neovim/NvChad | How to Close Neovim/NvChad]]
- [[How To Use Vim or Neovim#Saving a File | Saving a File]]
- [[How To Use Vim or Neovim#Saving and Closing a File | Saving and Closing a File]]

---

# Opening Neovim/NvChad

## On Windows:

### Opening Through Graphical User Interface ( GUI )

To open Neovim/NvChad, there are a few ways we could do this.

When you installed Neovim, a *.exe* file will appear when you press the start/super button.
Thus you can search for "Neovim" and you can start using it.

>[!warning]
>This will **not** open *NvChad*.

### Opening Through Command Line Interface ( CLI )

### Regular Powershell

To open Neovim/NvChad, we need to:

- Search for "Powershell" in the search bar
- Open powershell

After Powershell opens, type the following to use Neovim/NvChad

```powershell

nvim 

```


### Using Terminal and New Powershell from Microsoft Store

If you followed my Neovim installation guide; I recommended using *"Terminal"*.

To open Neovim/NvChad, we need to:

- Search for "Terminal" in the search bar
- Open Terminal

After Terminal opens, type the following to use Neovim/NvChad

```powershell

nvim

```

## On Linux

To open Neovim/NvChad on Linux, we need to 

- Open the terminal and type the following commands:

```bash

nvim

```

## On Mac OS

To open Neovim/NvChad on Mac OS, we need to

- Open the terminal and type the following commands:

```bash

nvim

```

---

# How to Close Neovim/NvChad


To close we need to type the following:

```vim

:q

```

This will quit the Neovim/NvChad.
If you have opened for example: the file tree, to *close* **Neovim** we need to first exit the file tree and then quit Neovim

So basically we need to type ":q" two times.

# Saving a File 

To save a file we need to type the following:

```vim

:w

```

The following folder will save the current file that you are working with in Neovim

In **NvChad**, we can also user *"Ctrl + S"* to save a file like other applications ( Notepad, Microsoft Word, etc  )

## Saving and Closing a File 

To save and quit a file at the same time, type the following 

```vim

:wq

```

## Quit Without Saving/Without Making Any Changes

To close a file **without** saving, we need to type the following:

```vim

:q!

```

This also works if we wrote something into the file and then realised that we did not need to write anything. By using the command above; the file will revert back to its original state.

---

# NvChad 

NvChad has a **cheat sheet** which can be accessed by pressing the leader key + ch  

>[!note] 
>The default **leader** key is *space* in NvChad

There you will find most used keymaps. Again these keymaps can be changed in the *.lua* files.
Please take a look at the cheatsheet because it has important things that you will want to use.

For example: Did you know that you can **find files** inside of *NvChad*