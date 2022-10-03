# Python Scripting

## Learning Goals

- Learn about scripting.
- Write a script in python.

***

## Key Vocab

- **Module**: a file containing Python definitions and statements. A module's
functions, classes, and global variables can be accessed by other modules.
- **Package**: a collection of modules that can be accessed as a group using
the package name.
- **`import`**: the Python keyword used to access data from other packages and
modules inside of the current module.
- **PyPI**: the **Py**thon **P**ackage **I**ndex. A repository of Python
packages that can be downloaded and made available to your application.
- **`pip`**: the command line tool used to download packages from PyPI. `pip`
is installed on your computer automatically when you download Python.
- **Virtual Environment**: a collection of modules, packages, and scripts that
can be activated or deactivated at any time.
- **Pipenv**: a virtual environment tool that uses `pip` to manage the modules,
packages, and scripts that you intend to use in your application.

***

## Introduction

The word script in the context of programming refers to a code file containing a program which usually executes
some tasks that need to be automated. Scripts are meant to be directly executed by the users.

How are scripts different than the modules we write in python?

Code that is meant to be imported and used in another program is a module.
Script are meant to be run directly.

***
## Shebang

## if __name__ == "__main__":

```py
if __name__ == "__main__":
    # do things
```

You may have seen this syntax before when working with python or looking at python examples.
This tells python that you only want to run the the code if the program is executed as a standalone file.
If we import the script into another program the code in the if statement will not run because the
`__name__` variable will not be equal `"__main__"`.

***

## Accepting arguments form command line

Using the sys module we can accept inputs from the user from the command line.
Lets use the `sys.argv` list which allows us to get input from the user and print it.

Lets look at the following script

```py
import sys
# The user input starts at index 1 in the sys.argv list. 
name = sys.argv[1]
if __name__ == "__main__":
    print(f"The name is {name} ")
```

We can run this script in the terminal using the following command

```bash
$ python bin/script.py Steve
The name is Steve 
```

## Using os.system to Run a shell command

We can also run shell commands using the `os` module
Lets try to use the `ls -l` shell command in our script.

```py
import os
if __name__ == "__main__":
    os.system('ls -l')
```

The script will give us a list of files that are in the current directory.

```bash
$ python bin/script.py
-rw-r--r--  1 user  staff  1810 Jul 28 19:23 CONTRIBUTING.md
-rw-r--r--  1 user  staff  1346 Jul 28 19:23 LICENSE.md
-rw-r--r--@ 1 user  staff  3653 Sep 27 22:30 README.md
drwxr-xr-x  3 user  staff    96 Sep 27 21:53 bin
```

## Conclusion

We have covered some introductory concepts in scripting. You have learned how to accept
inputs from the users and run system commands in a script. These tools can help us become
much more productive by automating tasks and procedures.

***

## Resources

- [Python](https://docs.python.org/3/)
- [Python os.system](https://docs.python.org/3/library/os.html#os.system)
- [Python sys](https://docs.python.org/3/library/sys.html)
