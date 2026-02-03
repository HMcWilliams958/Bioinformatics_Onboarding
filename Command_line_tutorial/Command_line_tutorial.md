## Command Line Basics Tutorial (20 minutes)

Welcome! You're about to learn the fundamentals of navigating and managing files using the command line. This tutorial is self-paced and hands-on — type each command into your terminal and observe what happens.

### What You'll Learn
- Print your current working directory (`pwd`)
- List files and folders (`ls`)
- Navigate between directories (`cd`)
- Create directories and files (`mkdir`, `touch`)
- Copy, move, and delete files (`cp`, `mv`, `rm`)
- Use flags to modify command behavior
- Access help documentation (`--help`, `man`)

### Getting Started

**Step 1: Know Where You Are (2 minutes)**

Your terminal always has a "current working directory" — a location in your file system where commands are executed. Let's find out where you are:

```bash
pwd
```

You'll see a path like `/c/Users/harri` (Git Bash shows paths in Unix-style format). This is your home directory.

**Step 2: See What's Around You (2 minutes)**

List all files and folders in your current directory:

```bash
ls
```

You'll see a list of folders like `Desktop`, `Documents`, `Downloads`, etc. To see hidden files too (files starting with a dot), use a flag:

```bash
ls -a
```

The `-a` flag means "all" — it modifies `ls` to show everything. Flags always start with a dash and change how a command behaves.

Want more details about each file? Try:

```bash
ls -l
```

The `-l` flag means "long format" and shows file sizes, dates, and permissions. Combine flags:

```bash
ls -la
```

**Step 3: Navigate to a Different Directory (3 minutes)**

Move into your `Documents` folder:

```bash
cd Documents
```

Check where you are now:

```bash
pwd
```

You should see something like `/c/Users/harri/Documents`. Now list what's inside:

```bash
ls
```

Go back up one level to your home directory:

```bash
cd ..
```

The `..` means "parent directory" (the folder that contains the current folder). Check your location:

```bash
pwd
```

You're back in your home directory. You can also jump directly to your home directory from anywhere by typing:

```bash
cd ~
```

The `~` is a shortcut for your home directory.

**Step 4: Create a Practice Workspace (3 minutes)**

Let's create a folder to practice in. First, navigate to your `Documents` folder:

```bash
cd Documents
```

Create a new directory called `CLI_Practice`:

```bash
mkdir CLI_Practice
```

The `mkdir` command means "make directory." Navigate into it:

```bash
cd CLI_Practice
```

Verify you're inside:

```bash
pwd
```

**Step 5: Create and Manage Files (5 minutes)**

Create an empty file:

```bash
touch file1.txt
```

Create a few more files:

```bash
touch file2.txt file3.txt
```

List them:

```bash
ls
```

**Copying files:** Create a copy of `file1.txt`:

```bash
cp file1.txt file1_backup.txt
```

List to confirm:

```bash
ls
```

**Moving (renaming) files:** Rename `file2.txt` to `notes.txt`:

```bash
mv file2.txt notes.txt
```

**Deleting files:** Remove `file3.txt`:

```bash
rm file3.txt
```

List again:

```bash
ls
```

**Note:** `rm` permanently deletes files — no undo. Be careful!

**Step 6: Tab Completion (2 minutes)**

Typing long names is slow. Use **Tab** to autocomplete. Try this:

```bash
ls file
```

Now press **Tab**. The terminal will complete it to `file1.txt` (or prompt you if multiple matches exist). This saves time and prevents typos. Try it:

```bash
cp file1
```

Press **Tab** — it autocompletes. Then add a space and type the destination:

```bash
cp file1_backup.txt file1_copy.txt
```

**Step 7: Understand Flags and Help (3 minutes)**

You've already used flags like `-a`, `-l`, and `-la`. Let's learn more. List your directory with human-readable file sizes:

```bash
ls -lh
```

The `-h` flag means "human-readable" (shows KB, MB, etc. instead of raw bytes).

**Get help on any command:**

```bash
ls --help
```

You'll see all flags available for `ls`. Try:

```bash
mkdir --help
```

or

```bash
cp --help
```

Some systems support `man` pages (manual pages) for detailed documentation:

```bash
man ls
```

Press `q` to exit the manual.

### Review: Key Commands Cheat Sheet

| Command | What It Does | Example |
|---------|-------------|---------|
| `pwd` | Print working directory | `pwd` |
| `ls` | List files | `ls` or `ls -la` |
| `cd` | Change directory | `cd Documents` or `cd ..` |
| `mkdir` | Make directory | `mkdir my_folder` |
| `touch` | Create empty file | `touch file.txt` |
| `cp` | Copy file | `cp file.txt copy.txt` |
| `mv` | Move or rename | `mv old.txt new.txt` |
| `rm` | Remove file | `rm file.txt` |
| `--help` | Get command help | `ls --help` |

### Challenge (Optional)

1. Create a folder called `my_project` in your `CLI_Practice` directory.
2. Create three files inside it: `readme.txt`, `script.sh`, `data.csv`.
3. Copy `data.csv` to `data_backup.csv`.
4. Rename `script.sh` to `main.sh`.
5. Delete `readme.txt`.
6. List all files to confirm.

**You've completed the command line basics!** You now understand how to navigate, create, copy, move, and delete files using the terminal. These are fundamental skills for programming, HPC work, and version control with Git.
