# 0x00. AirBnB clone - The console

![HolBnB clone](./hBnB.png)
Welcome to the AirBnB clone project!

## Getting Started

**First step: Write a command interpreter to manage your AirBnB objects.**

This is the first step towards building your first full web application: the AirBnB clone. This first step is very important because you will use what you build during this project with all other following projects: HTML/CSS templating, database storage, API, front-end integration…

Each task is linked and will help you to:

- put in place a parent class (called `BaseModel`) to take care of the initialization, serialization and deserialization of your future instances

- create a simple flow of serialization/deserialization: Instance <-> Dictionary <-> JSON string <-> file
- create all classes used for AirBnB (`User`, `State`, `City`, `Place`…) that inherit from `BaseModel`
- create the first abstracted storage engine of the project: File storage.
- create all unit tests to validate all our classes and storage engine

**What’s a command interpreter?**

Do you remember the Shell? It’s exactly the same but limited to a specific use-case. In our case, we want to

be able to manage the objects of our project:

- Create a new object (ex: a new User or a new Place)

- Retrieve an object from a file, a database etc…

- Do operations on objects (count, compute stats, etc…)

- Update attributes of an object

- Destroy an object

### Learning Objectives

## General

- How to create a Python package
- How to create a command interpreter in Python using the `cmd` module

- What is Unit testing and how to implement it in a large project

- How to serialize and deserialize a Class

- How to write and read a JSON file

- How to manage `datetime`

- What is an `UUID`

- What is `*args` and how to use it

- What is `**kwargs` and how to use it

- How to handle named arguments in a function

## Execution

Your shell should work like this in interactive mode:

```Python
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF help quit

(hbnb)
(hbnb)
(hbnb) quit
$
```

But also in non-interactive mode: (like the Shell project in C)

```Python
$ echo "help" | ./console.py

(hbnb)

Documented commands (type help <topic>):
========================================

EOF help quit
(hbnb)
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)


Documented commands (type help <topic>):
========================================
EOF help quit
(hbnb)
$

```

All tests should also pass in non-interactive mode: `$ echo "python3 -m unittest discover tests" | bash`

## Tasks

## 0. README, AUTHORS

- Write a `README.md`:

  - description of the project
  - description of the command interpreter:
    - how to start it
    - how to use it
    - examples

- You should have an `AUTHORS` file at the root of your repository, listing all individuals having contributed content to the repository. For format, reference [Docker’s AUTHORS page](https://github.com/moby/moby/blob/master/AUTHORS)

- You should use branches and pull requests on GitHub - it will help you as team to organize your work

## 1. Be pycodestyle compliant!

Write beautiful code that passes the pycodestyle checks.

## 2. Unittests

All your files, classes, functions must be tested with unit tests

```Python
guillaume@ubuntu:~/AirBnB$ python3 -m unittest discover tests
...................................................................................
...................................................................................
.......................
----------------------------------------------------------------------
Ran 189 tests in 13.135s

OK
guillaume@ubuntu:~/AirBnB$
```

Note that this is just an example, the number of tests you create can be different from the above example.

**Warning:**

Unit tests must also pass in non-interactive mode:

```Python
guillaume@ubuntu:~/AirBnB$ echo "python3 -m unittest discover tests" | bash
...................................................................................
...................................................................................
.......................
----------------------------------------------------------------------
Ran 189 tests in 13.135s

OK
guillaume@ubuntu:~/AirBnB$
```

## 3. 3. BaseModel
