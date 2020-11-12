# Today we learned about text editors, Termial and installed Git, Visual Studio Code and other software with Terminal

## Text Editors

A Text Editor is apiece of Software on your computer or on the web that allows you to write and manage text. The text editor is one of the most important tools you can use as a developer, so its important to pick the right one that works for you.

### Cool Features to look out for in a *Text Editor*

1. **Code Completion:** Shows possible suggestions when you start typing code.
2. **Syntax Highlighting:** Colorizes text to make it easier to read.
3. **Varied Themes:** Lets you change the color of background and text.
4. **Extensions Availability:** Lets you add certain functionalities that you might need (Boiler-plate).
5. **EMMET:** A kind of shorthand that helps you code faster.

### Some Examples of code editors

There are several kinds of text editors to choose from, here are a few:
- **Notepad++**; For Windows only.
- **BB Edit**; Free version works like *Text Wrangler*, you can pay for more features.
- **Visual Studio Code**; Free for Windows, MAC, Linux and has EMMET built in (we downloaded this one :smiley: ).
- **Atom**; Free for Windows, Mac, Linux.
- **Brackets**; Free on all platforms. Mostly good for basic coding without exetensions.

### Text Editors vs IDE's
*Text Editors* manage texts and files while *IDE's* (Intergrated Development Environment) is a file manager, a compiler and a debugger all in one software.

## Terminal

Terminal is the command line interface, a barebones way to navigate and instruct the computer what to do. As oppesed to the graphic user interface which is what most people use to navigate a computer.

### A few Terminal commands

#### CORE COMMANDS
```
cd:	Home directory
cd: [folder]	Change directory
cd ~:	Home directory, e.g. ‘cd ~/folder/’
cd /:	Root of drive
ls:	Short listing
ls -l:	Long listing
ls -a:	Listing incl. hidden files
ls -lh:	Long listing with Human readable file sizes
ls -R:	Entire content of folder recursively
sudo [command]:	Run command with the security privileges of the superuser (Super User DO)
open [file]:	Opens a file
open .:	Opens the directory
top	Displays active processes.: Press q to quit
nano [file]:	Opens the Terminal it’s editor
pico [file]:	Opens the Terminal it’s editor
q:	Exit
clear:	Clear screen
```
#### FILE MANAGEMENT
```
*touch [file]*:	Create new file
*pwd*:	Full path to working directory
*..*:	Parent/enclosing directory, e.g.
*ls -l ..*:	Long listing of parent directory
*cd ../../*:	Move 2 levels up
*.*:	Current folder
*cat*:	Concatenate to screen
*rm [file]*:	Remove a file, e.g. rm [file] [file]
*rm -i [file]*:	Remove with confirmation
*rm -r [dir]*:	Remove a directory and contents
*rm -f [file]*:	Force removal without confirmation
*rm -i [file]*:	Will display prompt before
*cp [file] [newfile]*:	Copy file to file
*cp [file] [dir]*:	Copy file to directory
*mv [file] [new filename]*:	Move/Rename, e.g. mv -v [file] [dir]
```
### DIRECTORY MANAGEMENT
```
*mkdir [dir]*:	Create new directory
*mkdir -p [dir]/[dir]*:	Create nested directories
*rmdir [dir]*:	Remove directory ( only operates on empty directories )
*rm -R [dir]*:	Remove directory and contents
```
