
# TERMINAL NAVIGATION

---

Title: Lesson 2<br>
Duration: ~ 1.25 hrs<br>
Creator: Thom Page for WDIR<br>
Modified by: Karolin Rafalski for DSR <br>
Note: Some resources from original DSR source material also adapted
Topics: Intro, Terminal, "Hello World"<br>

---

## Intro

Hello, you are reading the intro.

Today we will use `markdown` to share lesson notes.  Markdown is a very simple text formatting language that can be rendered on github, in many text editors and more! After today's lesson, you will likely get your lesson notes via Jupyter Notebook.

Day to day:

- Lesson headers
	- Headers will be posted for all lessons and labs with links to markdowns and the Zoom channel.
- Markdown
	- Markdown/Jupyter notebooks contain reference material related to the lesson
	- Slides from the markdown will be posted into Slack during the lesson ![](https://i.imgur.com/xxs7w7f.png)
- Sharing screen
	- The instructor will screenshare for demonstration purposes. Double-click out of fullscreen.
- Screen real-estate: markdown, zoom, text editor, terminal, slack
	- Command-tab to cycle applications
- Muting
	- Be muted unless speaking
- Asking questions
	- Ask away! Either in Slack or out loud
- Visibility of instructor code
	- Speak up if the instructor's code is not visible (eg. too small).
- Thumbsups
	- We use the thumbsup emoji (or in this case the Gizmo / Gremlin emojis) to gauge completeness of exercises. Click on the thumb or Gizmo or Gremlin when you are done with an exercise.


<br>
<hr>

## Software

- Atom installed? Or your favorite text editor
	- [Download Atom](https://atom.io/)
  - [Download Submlime](https://www.sublimetext.com/download)
- [Login to Github Enterprise](https://git.generalassemb.ly)
- Shared username with online@generalassemb.ly , so  you may have access to the class repositories
- Python 3.6 installed
- If you are NOT using a MAC, [git bash](http://gitforwindows.org/)
- Get ready for next session: Download and install [Anaconda](https://www.anaconda.com/download)

<br>
<hr>

## Lesson Objectives

_After this lesson, students will be able to:_

* Use Terminal to navigate files and folders
* Create files and folders on the command line
* Navigate using relative pathing on the command line
* Print a "Hello World" to the console

<br>
<hr>

## Terminal

### Intro to the Command Line

#### What is a GUI?
There was a time when computers didn't come with a graphical user interface (GUI, pronounced "gooey"). Instead, everyone interacted with the computer using text commands in what we call a command-line interface (CLI).

![wikimedia image of cli](https://git.generalassemb.ly/datr1618/your-development-environment/raw/5714588ca395eaf9b66d76c13f6fab3ce1ebc7dc/assets/dos_wikimedia.png)

Today, the command line still exists, even though you may have never seen it as a casual computer user. However, knowing basic CLI commands is a useful skill.

This CLI is the gateway to your operating system and can perform many of the same actions without a graphical interface. It is also facilitated by what we call a "shell."

Just for fun! Show your friends and family you are now a fast paced super hacker, just [go here](http://hackertyper.com/) and randomly hammer away at the keyboard

#### What is a Shell?
A shell is a type of command-line program that contains a simple, text-based user interface, enabling us to access all of an operating system's services. It is, put simply, a program that accepts text as an input and translates that text into the appropriate functions you want your computer to run.

Running applications, checking settings such as free hard drive space, and even web browsing can all happen from the shell.

DEMO - no need to code along (we'll do this together again at the end of the lesson)
We can open a python shell by typing in bash
 - `python` - notcie the prompt will change from a `$` to a `>>>`
 - `x = 'Hello world!'`
 - `print(x)`
 - `exit()` - prompt returns to `$`


Windows Users

In this class, we will use a popular UNIX shell called bash. If you have not already, we recommend installing Git Bash.

What Is Git Bash? Git Bash provides a set of executables that emulate bash commands in the Windows shells.

Why? Since UNIX is the prefered operating system for programmers and developers alike, almost all of the lessons at GA have been written for interaction with UNIX.

Pro Tip: UNIX commands and Windows commands are not polar opposites — in fact, most of their commands and interactions are quite similar.

&#x1F535; **Open Terminal**

- `⌘ (Command) + Space`, or open Spotlight
- "*Te*rminal"
- `Enter`

![](https://i.imgur.com/CvggrYa.png)

- Keep it locked in your dock. Right click on the icon, highlight options, check "Keep in Dock".

![](https://i.imgur.com/ZrPuVNq.png)


&#x1F535; **Terminal Preferences**

You can change the color of your Terminal and the font size. It is recommended to make your Terminal output easier to read, rather than the tiny default output.

> Terminal > Preferences > Pro

<br>
<hr>


## Terminal as Our Command Line Interface

Terminal provides a Command Line Interface (CLI) to the operating system. With it you can give your computer direct, text-based instructions. It is the most powerful piece of software on your computer! Think of it as the central hub of your development process. For now, we will use it to navigate the files and folders in our computer.

When terminal launches, it will start in your computer's home directory (whatever you named your computer). Your home directory is denoted by the tilde `~`.

In Terminal-land, **Directories** are the same as **Folders** (we just call them **Directories**).

![](https://i.imgur.com/tTyOkwV.png)


In **Finder**, we can also navigate our computer's folders and files: folders contain files and more folders:

![](https://i.imgur.com/CR7PmAO.png)

<br>

## Bash Commands

The Command Line understands commands written in the `bash scripting language`. The commands are abbreviations of English words, or acronyms.

- `pwd` - will print the current working directory. It shows you a `path`. This `path` shows you where are curently located in the filesystem. It's like sending up a flare or homing beacon, where you can see how far you have 'traveled' from the root directory.

![](https://i.imgur.com/4aaT88x.png)

- `ls` - Lists the contents of the current directory. You can see
	* the  immediate _child_ directories (the directories inside this directory)
	* the files and directories that are not hidden.

![](https://i.imgur.com/H2RTUny.png)

- Bash commands can take `flags` denoted by a dash `-`
	- `ls -a` - list content including hidden files and directories. Hidden files and directories begin with a period, for example, `.git`.


Directories (folders) can have directories within them, and there can be directories inside _those_ directories, ad infinitum. This creates a tree structure where directories can have many children with many different branches.

![](http://i.imgur.com/M6OgKZJ.png)

<br>
<hr>

## Paths
Every file or folder in a file system can be read, written, and deleted by referencing its position inside that system. When we talk about the position of a file or a folder in a file system, we refer to its "path." There are two different kinds of paths we can use to refer to a file — absolute paths and relative paths.


#### What Is an Absolute Path?
All files can created, updated, or deleted using the command line interface. We do this by referencing paths; either relative or absolute.

An absolute path is the specific location of a file or folder as accessed from the root directory, typically shown as /. The root directory is the starting point from which all other folders are defined and is not usually the same as your home directory, which is normally found at /Users/[Your Username].


#### What Is a Relative Path?
A relative path is a reference to a file or folder relative to your current position or the present working directory (pwd). If we are in the folder /a/b/ and we want to open the file that has the absolute path /a/b/c/file.txt, we can simply type:

> open c/file.txt

or

> open ./c/file.txt

We can also use the absolute path at any time by adding a slash to the beginning of the relative path. The absolute path is the same for a file or a folder, regardless of the current working directory, but relative paths differ based on directory. Directory structures are laid out like so: directory/subdirectory/subsubdirectory.

Check: What is the difference between an absolute path and a relative path?


## CHANGING DIRECTORIES

We can navigate to other directories _relative_ to the current working directory.

- `cd some_directory`
	- navigates into a child directory called `some_directory`. `some_directory` is a child of the current directory.
- `cd ..`
	- navigates into the parent of the current directory
	- `..` is shorthand for parent
- `cd` will take you back home

**Shortcuts**

- letter[TAB]
	- autocompletes (case-sensitive)

- up / down arrow
	- cycle command history

<br>

&#x1F535; **Code Along (2 min)**

* From the home directory, navigate to Library
* Pick a directory and navigate to the end with `cd directoryname`. Remember to autocomplete.
* Then navigate back up with `cd ..`
* Navigate to Library
* Pick a directory and navigate to the end
* Navigate back home with `cd`

<br>
<hr>

12:35

## Terminal Keyboard shortcuts

In the long term, reduce your reliance on the mouse. More Bash keyboard shortcuts:

`⌘ K` Clear the Terminal window

`option arrow` Move cursor by word

<br>
<hr>

## MAKING DIRECTORIES AND FILES

`mkdir` - makes a directory

Example:

- `mkdir directory_name`

	> makes a directory called 'directory_name'`

<br>

`touch` - creates an empty file. A file typically will have a **file extension** like `.txt` whereas a directory will not.


Example:

- `touch file.txt`

	> makes a .txt file

<br>

&#x1F535; **Code Along (4 min)**

* Navigate home `cd`
* Go to Documents
* Make directory `exercise`
* Go into the directory with autocomplete
* Make two directories `example1` and `example3` and list them
* Go into `example1` with autocomplete
* Make two directories on a single line, `example3` and `example4`
* Go into `example3` and make a file `file1.txt`
* List the file
* Navigate back to exercise

<br>

&#x1F535; **Activity (10 min)**

**Construct a Labyrinth**

Using what you know about navigating directories and creating files and folders, construct a 'labyrinth' on your desktop.

**Precision** is important. There are a few layers to this exercise. Be patient.

- Make sure you are in the correct directory when you go to create another directory or file.
- Make sure you use `touch` to make files, and `mkdir` to make directories. **files** and **directories** are two different things.

* Navigate to Desktop
* `mkdir Labyrinth`, `cd Labyrinth`
* Make a directory structure like this:

![labyrinth](https://i.imgur.com/V1zaeBT.png)

**parlor** and **stairway** are _child directories_ of the Labyrinth directory.

**sarah_williams.txt** is a _file_ inside the the ballroom directory.

If you make a mistake, don't worry, just keep adding the right stuff to the right place.


<br>
<hr>
12:50
<br>

## Navigation: RELATIVE PATHING

Chain more directories to the current path with the `/` separator

- Go down the chain into child directories
	- `cd parent_directory`
	- `cd parent_directory/child_directory`
	- `cd parent_directory/child_directory/grandchild_directory`

- Go up the chain into parent directories
	- `cd ..`
	- `cd ../..`
	- `cd ../../..`

- Go sideways into a _sibling_ directory by first going up, then down
	- `cd ../sibling_directory`

- Go into an _aunt_ or _uncle_ directory by first going up to the parent, then the grandparent, then down again on another branch:

	- `cd ../../auntie_directory`

<br>

&#x1F535; **Code along (2 min)**

**Navigate the Labyrinth**

* Navigate to the Labyrinth root directory
* From the Labyrinth root directory, navigate to the `stairway`
* From the `stairway`, navigate to the `parlor`
* From the `parlor`, navigate to the `dining room`
* From the `dining room`, navigate to the `escher room`
* From the `escher room`, navigate to the Labyrinth root

<br>

&#x1F535; **Activity (10 min)**

**Navigate the Labyrinth**

For each of these, write your command on one line, using full paths:

* Navigate to the Labyrinth root directory
* From the Labyrinth root directory, navigate to the `dining_room`
* From the `dining room`, navigate back up the root directory
* From the Labyrinth root directory, navigate to the `stairway`
* From the `stairway`, navigate to the `parlor`
* From the `parlor`, navigate to the `escher_room`
* From the `escher room`, navigate to the `throne_room`
* From the `throne_room`, navigate to the `ball_room`

<br>
<hr>

## (Extra) Navigation: ABSOLUTE PATHING

Move anywhere relative to the home directory:

`cd ~/` - the path starts in home directory

Example:

- `cd ~/Desktop/Labyrinth/stairway/escher_room`

Navigates to the escher room _no matter where_ you are currently located in your filesystem

> NOTE: You can combine absolute and relative pathing when copying or moving files from one location to another with `cp` and `mv`.

<br>

&#x1F535; **Activity (3 min)**

**Navigate the Labyrinth**

Using absolute pathing:

* Navigate to the throne_room
* Navigate to the ballroom
* Navigate to the parlor



<br>
<hr>

# Code

We are going to:

* make a file
* open it in our text editor
* write some code
* run the code in Terminal

&#x1F535; **Code Along (5 min)**

* In Terminal, navigate to Documents.

* Make a directory `w1d1_student_examples`

* Go inside the directory

* Make a file `first_code.js`

* Open up Atom, either by typing `atom` or doing it manually through Spotlight or the Dock.

* Go to `Atom -> Install Shell Commands`

![](https://i.imgur.com/AqFki3f.png)

* Close Atom

* From inside the `w1d1_student_examples` directory, open Atom from the command line with `atom .` (atom space dot)

**NOTE** This might not work on some systems. If not we will get it sorted out in time. For now, Just open the directory from `File -> Open`, and open the `w1d1_student_examples` directory.

* When Atom opens, you should see the `w1d1_student_examples` directory and all the files inside the directory (in this case, just the `first_code.js` file.

<br>
<hr>

You can dive deeper by checking out `Your-Development-Environment.ipynb`


## More Terminal Keyboard shortcuts

In the long term, reduce your reliance on the mouse.
More Bash keyboard shortcuts:

`⌘ K` Clear the Terminal window

`option arrow` Move cursor by word

`Ctrl A` Go to beginning of line

`Ctrl E` Go to end of line


`Ctrl K` Kill line to end

`Ctrl U` Kill line to beginning

`Ctrl Y` Yank clipboard to line


`cd -` toggle previous directory



<br>
<hr>
