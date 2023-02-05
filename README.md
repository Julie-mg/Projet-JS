# Projet-JS

## main.js

This code is a test of a shell program in JavaScript. It manages the modifications of the current file and print it on the terminal as well as other commands listed just below.

The valid commands :

_lp_ : Listing of all running processes

_cd_ : Change the current directory, to the previous one, a next one... (example : /mnt/c/../c/.. is correctly managed)

_bing [-k|-p|-c] <PID>_ : Stopping, killing, or continuing a process

_keep <PID>_ : Detaching a process with the 'keep <PID>' command (we're having some issues with this one as the processes don't stay in background as soon as we close the terminal which was launching them, but we managed to put them in background with the `nohup <command> &` command)

_<name_program> !_ : Run a command in the background

all the other bash/sh commands are also available and managed

The code is infinitly waiting for incomming data from the terminal (`process.stdin.on()`). This is causing issues to implement the Ctrl+P required command as the program isn't waiting for just one keyboard key to be pressed. If so, each key pressed will try to launch a command, which will be impossible to manage to read string from the terminal.

### Launching this code

To start to use this program, you need to follow these steps :

* download the `Main.js` file

* open a Linux terminal in the repository of the downloaded file

* run `node main.js`
