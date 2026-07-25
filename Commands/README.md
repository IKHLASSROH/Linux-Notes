# picoCTF - General Skills (Day 1)

Today I built a stronger foundation in Linux and cybersecurity by solving beginner-friendly picoCTF General Skills challenges. I learned how to navigate Linux, analyze files, use command-line tools, and approach CTF challenges methodically.

---

# Challenges Solved

- ✅ Lets Warm Up
- ✅ Wave a Flag
- ✅ Nice netcat...
- ✅ strings it
- ✅ Based
- ✅ Python Wrangling
- ✅ First Find
- ✅ Static ain't always noise
- ✅ What's a Pipe?
- ✅ grep

---

# Linux Fundamentals

## Navigation

### `pwd`

Displays the current working directory.

```bash
pwd
```

### `ls`

Lists files and directories.

```bash
ls
```

Useful options:

```bash
ls -a
```

Shows hidden files and directories.

---

### `cd`

Changes the current directory.

```bash
cd Downloads
```

Go back one directory:

```bash
cd ..
```

---

# Reading Files

### `cat`

Displays the contents of a file.

```bash
cat password.txt
```

---

# Searching

## `grep`

Searches for text inside files or command output.

```bash
grep pico file
```

Search command output:

```bash
strings file | grep pico
```

---

## `find`

Searches for files and directories.

```bash
find . -name uber-secret.txt
```

Explanation:

- `.` → search from the current directory
- `-name` → search by filename

---

# Pipes

## Pipe (`|`)

Passes the output of one command directly into another command.

Example:

```bash
strings file | grep pico
```

Flow:

```
strings
     │
     ▼
 readable text
     │
     ▼
grep
     │
     ▼
matching lines
```

Pipes are one of the most useful Linux features for combining commands.

---

# Binary Analysis

## `strings`

Extracts readable text from binary files.

```bash
strings file
```

Search directly for the flag:

```bash
strings file | grep picoCTF
```

---

# Networking

## Netcat (`nc`)

Connects to remote services.

Syntax:

```bash
nc hostname port
```

Example:

```bash
nc fickle-tempest.picoctf.net 61440
```

Using a pipe:

```bash
nc hostname port | grep picoCTF
```

---

# Python

Run a Python script:

```bash
python3 script.py
```

Example:

```bash
python3 ende.py -d flag.txt.en
```

Meaning:

- `python3` → Python interpreter
- `ende.py` → Python program
- `-d` → decrypt mode
- `flag.txt.en` → encrypted file

---

# Linux Executables

Give execute permission:

```bash
chmod +x filename
```

Run the executable:

```bash
./filename
```

---

# Downloading Files

Use `wget` to download files.

```bash
wget URL
```

---

# Getting Help

Display help:

```bash
command --help
```

or

```bash
command -h
```

Manual pages:

```bash
man command
```

Examples:

```bash
man grep
man find
man python3
```

---

# Hidden Files

Linux files beginning with `.` are hidden.

Example:

```
.secret
```

View hidden files:

```bash
ls -a
```

---

# Files vs Directories

A directory:

```bash
cd folder
```

A file:

```bash
cat file.txt
```

You cannot use `cd` on a regular file.

---

# Number Systems

Learned the basics of:

- Decimal (Base 10)
- Binary (Base 2)
- Hexadecimal (Base 16)

Practiced converting between all three systems.

---

# ASCII

Converted decimal and hexadecimal values into ASCII characters.

Example:

```
112 -> p
105 -> i
99  -> c
111 -> o
```

Result:

```
picoCTF{...}
```

---

# Basic Cryptography

Learned the difference between:

- Encryption
- Decryption

Also got an introduction to:

- XOR
- Encoded data
- Encrypted files

---

# Problem Solving Skills

During these challenges I learned to:

- Read challenge descriptions carefully.
- Read hints before guessing.
- Break problems into smaller steps.
- Search files efficiently.
- Search directories recursively.
- Analyze binaries without executing them.
- Connect to remote challenge servers.
- Combine Linux commands using pipes.
- Understand what each command actually does instead of memorizing it.

---

# Commands Learned

```text
pwd
ls
ls -a
cd
cat
grep
find
strings
wget
chmod +x
./file
python3
nc
man
```

---

# Key Takeaways

- Linux commands become much more powerful when combined together.
- Reading challenge instructions carefully is often more important than knowing many commands.
- CTFs are about investigation, experimentation, and logical thinking.
- Understanding *why* a command works is far more valuable than memorizing syntax.
- Every solved challenge teaches a new tool or technique that can be reused in future challenges.

---

# Reflection

Today I strengthened my Linux and cybersecurity foundations through hands-on practice with picoCTF. Instead of memorizing solutions, I focused on understanding how each command works, why it works, and how different tools can be combined to investigate systems effectively. Every challenge improved my confidence in using the Linux terminal and reinforced the importance of curiosity, careful reading, and systematic problem-solving.
