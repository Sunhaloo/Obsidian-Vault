---
alias: Vim Motions
tag: nvim
date: 16-07-2023
---

---

## List Of Contents:



---

# Youtuber: [Vim Salesman](https://www.youtube.com/@vimsalesman)

The link to the video is [here](https://www.youtube.com/watch?v=hsFnJgmLOLk&t=49s)

# Modes

## Normal Mode

To go back to **normal** mode, we just need to press *escape*

```vim

<ESC>

```

Now, you will be able to use the **vim motions**

## Insert Mode

To *"type"* something into the file we need to enter **insert** mode.
To enter **insert** mode, we need to type: 

```vim

i 

```

**OR:** we can also use *"o"* or *"a"*

```vim

a

```

```vim

o

```

```vim

O

```

Once pressed, it will allow us to type into the file. 

>[!note]
>The *h-j-k-l* movement ( vim motions ) will **not** work in **insert** mode.

## Visual Mode

### Selecting Text from File

To select some text from file,use:

```vim

v

```

### Selecting Text by Lines

To select text **line** by **line**, use:

```vim

V

```

## Visual Block Mode

To enter **Visual Block Mode**, use:

```vim

Ctrl + V

```

When selecting, it will follow the *shape* of a **square**/**block**

## Deleting Selected Text

After selecting a some text we could remove it. To remove the selected lines, use:

```vim

d

```

## Copy Selected Text

To **copy** some text, use:

```vim

y

```

## Paste Selected Text

To **paste** some text, use:

```vim

p

```

---

# Moving Around in NORMAL Mode

## Moving Cursor ( Character by Character )

To move the cursor around in **normal** mode, we use the followings:

- k = up ( $\uparrow$ )
- j = down ( $\downarrow$ )
- h = left ( $\leftarrow$ )
- l = right ( $\rightarrow$ )

>[!warning]
>This will only work in **NORMAL** mode.

This is the equivalent to the arrow keys in other applications. But this is a better version as you do not need to lift your hand off the [home row](https://www.google.com/search?client=opera&hs=XS9&hl=en&sxsrf=AB5stBiQ41i5P7sfjZrKuF-CXrisrhjEjg:1689527220353&q=home+row+keyboard&spell=1&sa=X&ved=2ahUKEwj6v7qu25OAAxXSTqQEHS8IAfkQBSgAegQICBAB&biw=790&bih=859&dpr=1)

## Moving Cursor Word By Word

1. To move cursor by a word in the right direction ( $\rightarrow$ ); use the following in **normal** mode:

```vim

w

```

```vim

W

```

2. To move by a word in the right direction ( $\rightarrow$ ); use the following in **normal** mode:

```vim

b

```

```vim

B

```

## Moving Cursor from Start to End of a Sentence 

1. To place the cursor at the **end** of a sentence/line, use:

```vim

$

```

You will have to press: Shift + 4

2. To place the cursor at the **start** of a sentence/line, use:

```vim

0

```

## Moving Cursor from Braces ( Brackets, Square Brackets, Triangle Brackets )

To move the cursor from **bracket** to **bracket** ( frequently used in programming ), use:

```vim

%

```

You will have to press: Shift + 5

## Moving Cursor from Paragraphs or Blocks Of Text

To move from block of text to another, use:

```vim

{}

```

You will have to press: Shift + []

## Moving Cursor to First and Last Line of File

1. To move cursor to **first** line of file, use:

```vim

gg

```

2. To move cursor to **last** line of file, use:

```vim

G

```

---

# How to Close Neovim/NvChad


To close we need to type the following:

```vim

:q

```

This will quit the Neovim/NvChad.
If you have opened for example: the file tree, to *close* **Neovim** we need to first exit the file tree and then quit Neovim

# Saving a File 

To save a file we need to type the following:

```vim

:w

```

The following folder will save the current file that you are working with in Neovim

In **NvChad**, we can also user *"Ctrl + S"* to save a file like other applications ( Notepad, Microsoft Word, etc  )

## Saving and Duplicating the Contents a File to Another File with a Different Name

If you have a file and it has some text in it, and you want to make another file with the same contents as the **original** file but with a **different** *name*; use the following command:

```vim

:w "file_name"

```

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

---