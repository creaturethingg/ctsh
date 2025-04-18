# CTSH - CREATURETHINGG SHELL

> CTSH is a fast, lightweight, modular shell written in C++, made for Windows   
> It is extremely customisable and easy to add your own commands and modifications

```
ctsh "C:\\Dev\\ctsh\\shell" > ls
Listing directory '"C:\\Dev\\ctsh\\shell"'...
-> [DIR] "C:\\Dev\\ctsh\\shell\\commands"
-> [.EXE] "C:\\Dev\\ctsh\\shell\\ctsh.exe"
-> [DIR] "C:\\Dev\\ctsh\\shell\\help"
 
```

## Adding your own command   
Heres an example of adding a greet command   
`greet.cpp` : 
```
#include <iostream>

int main(int argc, char** argv) {
 std::cout << "Hello, " << argv[1] << std::endl;
}
```
Compile `greet.cpp -> greet.exe`   
Drag it to the `commands/` folder   
Optionally, add some documentation in `greet.txt`, and add it to the `help/` folder   
In CTSH, use
`> greet John`   
You should see   
`Hello, John`   
If you added documentation to the `help/` folder, you can use `help greet` to see the documentation   
As you can see, it is very simple to modify the shell   

## How to use it  
- Download and extract `package.zip`
- Locate `ctsh.exe`

With this exe file, you can add it to your PATH variables
or run it directly from there.  
In VSCODE, use `ctrl + shift + p` and go to `settings.json`   
Inside `"terminal.integrated.profiles.windows"`, add 
```
"CreatureThingg Shell": {
            "path": "path/To/Exe"
}
```

## READ ME.txt   
Here is a copy of the `READ ME.txt` file from  `package.zip`   


      
CTSH -- CREATURETHINGG SHELL

Created by https://github.com/creaturethingg

This is version 1.0 of CTSH

-----------------------------------------------

Although CTSH has many built-in commands (try "help all"),
the main purpose of it is that it's very modular and easy to 
extend. You can easily make your own commands and customise 
the shell just by dragging the files to a folder.

Note that currently, this shell only works on Windows

To create a command, add the executable to the commands folder.
The exe must have the same name as the command name and have the
.exe file extension. Optionally, add a text file explaining how
to use the command to the help folder. Now, you can use the 
command like '<x> <args..>' and get the documentation through
'help <x>'. 

The shell passes the arguments to the exe through 'argv'

BUILT IN COMMANDS:
  - cd
  - code
  - cp
  - exit
  - ls
  - mkdir
  - mv
  - ren
  - rm
  - run
  - scan

You can learn the built-in commands by using 'help all'
