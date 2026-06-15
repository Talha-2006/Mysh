# 🐚 Mysh (Custom UNIX Shell)

[![Language](https://img.shields.io/badge/Language-C-blue.svg)](https://en.wikipedia.org/wiki/C_%28programming_language%29)
[![Platform](https://img.shields.io/badge/Platform-Linux%20%7C%20macOS-lightgrey.svg)]()

A lightweight custom UNIX shell implementation written in C. This project serves as a functional command-line interpreter and demonstrates core systems programming concepts such as process creation, inter-process communication, piping, I/O redirection, background execution, and file descriptor manipulation.

## ✨ Features

* **Built-in Commands:** Supports common shell built-ins such as `cd`, `pwd`, and `exit`.
* **Program Execution:** Runs standard system programs such as `ls`, `grep`, `cat`, and more using `$PATH` resolution.
* **I/O Redirection:** Supports reading from files and writing output to files using `<`, `>`, and `>>`.
* **Piping:** Chains multiple commands together using `|`, passing the output of one command into the input of the next.
* **Background Processing:** Runs commands in the background using `&` without blocking the shell.
* **Signal Handling:** Handles interrupts such as `Ctrl+C` / `SIGINT` without crashing the shell.
* 
## ❗Source Code Notice

This project was completed as part of a university course. To comply with academic integrity policies, the source code is kept private. This repository is intended only to showcase the project’s purpose, features, and technical concepts.

## 🚀 Getting Started

### Prerequisites

You will need a UNIX-like operating system such as Linux or macOS with the following installed:

* `gcc` or `clang`
* `make`

### Installation and Compilation

Clone the repository:

```bash
git clone https://github.com/Talha-2006/mysh.git
cd mysh
```

Compile the shell:

```bash
make
```

Run the shell:

```bash
./mysh
```

## 💻 Usage Examples

Once inside the shell, you can run standard UNIX commands similar to how you would in `bash` or `zsh`.

### Standard Command Execution

```bash
> ls -la
```

### I/O Redirection

Write output to a file:

```bash
> echo "Hello, World!" > output.txt
```

Append output to a file:

```bash
> echo "Another line" >> output.txt
```

Read input from a file:

```bash
> cat < output.txt
```

### Piped Commands

```bash
> ls -l | grep "txt"
```

```bash
> ls -l | grep "txt" | wc -l
```

### Background Processes

```bash
> sleep 10 &
```

This runs the command in the background and immediately returns control to the shell.

## 🧠 Under the Hood

This shell was built using standard POSIX system calls to interact directly with the operating system.

### Process Management

The shell uses:

* `fork()` to create child processes
* `execvp()` to execute programs
* `wait()` and `waitpid()` to synchronize parent and child processes

### Piping and Redirection

The shell uses:

* `pipe()` to create communication channels between processes
* `dup2()` to redirect standard input and standard output
* File descriptors to manage input and output streams

### Command Parsing

The shell includes custom parsing logic to process user input, tokenize commands, identify special operators, and prepare arguments for execution.

## 🛠️ Technologies Used

* C
* POSIX system calls
* UNIX/Linux process management
* File descriptors
* Makefile-based compilation

## 📚 Concepts Demonstrated

This project demonstrates important operating systems and systems programming concepts, including:

* Shell design
* Process creation
* Parent and child processes
* Program execution
* Inter-process communication
* Input/output redirection
* Background jobs
* Signal handling
* File descriptor management

## ⚠️ Limitations

This shell is intended as a learning-focused UNIX shell implementation and may not support every feature found in production shells like `bash`, `zsh`, or `fish`.

Some advanced shell features may not be supported, such as:

* Command history
* Tab completion
* Environment variable expansion
* Quoting and escaping edge cases
* Advanced job control

## 👤 Author

**Talha Asif**

* GitHub: [@Talha-2006](https://github.com/Talha-2006)
* LinkedIn: [Talha Asif](https://www.linkedin.com/in/talhaasif06/)
