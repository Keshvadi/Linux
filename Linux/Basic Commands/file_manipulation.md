---
title: File Manipulation
parent: Basic Commands
nav_order: 22
layout: default
---

## File Manipulation

Efficient file manipulation is essential for effective control over files and directories within the Linux environment. This section covers fundamental commands for efficient file management in the Shell environment.

---

### `touch`

- Description: Creates an empty file or updates the timestamp of an existing file.

- Example usage:

  ```bash
  touch new_file.txt # Creates a new empty file named 'new_file.txt'
  touch existing_file.txt # Updates the timestamp of 'existing_file.txt'
  ```

**Note:** The touch command is versatile; it creates a new file if it doesn't exist or updates the timestamp of an existing file without altering its content. This command is useful for various file management tasks within the Linux system.

<!-- **Note**: A timestamp in computing refers to a record of when a file was last accessed or modified. -->

---

### `nano`

- Description: Opens the Nano text editor for creating or editing files within the terminal.

- Example usage:

  ```bash
  nano new_file.txt # Opens or creates a file named 'new_file.txt' for editing
  ```

**Note:** Nano text editor opens with a blank screen. Start typing your content. To save the file:

- Press `Ctrl + O` (Write Out) to save the file.
- Press `Enter` to confirm the filename.
- Press `Ctrl + X` to exit Nano.

---

### `cat`

- Description: Displays the content of a file or concatenates files and displays the output.

- Example usage:

  ```bash
  cat filename.txt # Displays the content of 'filename.txt'
  cat file1.txt file2.txt # Concatenates 'file1.txt' and 'file2.txt' and displays the output
  ```

**Note:** The cat command can be used to display the content of a single file or concatenate multiple files. This command is commonly used for file content analysis and manipulation.

---

### `echo`

- Description: Prints text or variables as output to the terminal.

- Example usage:

  ```bash
  echo "Hello, World!" # Prints "Hello, World!" to the terminal
  echo $USER # Displays the current user's username
  echo $HOME # Prints the path to the user's home directory
  echo $PATH # Shows the directories where executable files are located.

  export MY_VAR="Hello, Linux!" # Sets a custom variable MY_VAR
  echo $MY_VAR # Prints the content of MY_VAR
  ```

**Note:** The `echo` command in Linux is like the "_print_" function in programming languages. It is a fundamental command often used for displaying messages, variables, or strings within shell scripts or for general output in the command line.

---

### `>` (write)

- Description: Redirects command output and writes it to a file, creating a new file or overwriting an existing one.

- Example usage:

  ```bash
  cat file1.txt file2.txt > file3.txt
  echo "Hello, World!" > output.txt # Writes "Hello, World!" to 'output.txt'
  ```

---

### `<` (read)

- Description: Redirects input from a file to a command. It provides the command with the content of the file as input.

- Example usage:

  ```bash
    cat < input.txt # Provides 'cat' command with 'input.txt' content as input
  ```

**Note:** In this example, the `<` symbol for input redirection can be omitted. However, it becomes crucial in redirecting files within bash scripting (which you'll explore in the next session). Here's an example that you might not be able to execute now, but it's worth trying later when you learn bash scripting:

```bash
  while read line; do
      echo "Processing line: $line"
      # Perform operations with each line of input
  done < input_data.txt  # Explicit input redirection using '<'
```

---

### `cp`

- Description: Copies files or directories from one location to another.

- Example usage:

  ```bash
  cp file1.txt /destination/directory # Copies 'file1.txt' to '/destination/directory'
  cp -r directory1 directory2 # Copies 'directory1' and its content to 'directory2'
  ```

---

### `mv`

- Description: Moves or renames files or directories.

- Example usage:

  ```bash
  mv file1.txt newfile.txt # Renames 'file1.txt' to 'newfile.txt'
  mv file1.txt /destination/directory # Moves 'file1.txt' to '/destination/directory'
  ```

---

### `rm`

- Description: Removes (deletes) files or directories.

- Example usage:

  ```bash
    rm file1.txt # Deletes 'file1.txt'
    rm -r directory1 # Deletes 'directory1' and its content
  ```

---

### `head`

- Description: Displays the beginning lines of a file.

- Example usage:

  ```bash
    head filename.txt # Displays the first ten lines of 'filename.txt'
    head -n 5 filename.txt # Displays the first five lines of 'filename.txt'
  ```

---

### `tail`

- Description: Displays the ending lines of a file.

- Example usage:

  ```bash
  tail filename.txt # Displays the last ten lines of 'filename.txt'
  tail -n 5 filename.txt # Displays the last five lines of 'filename.txt'
  ```

<!-- ---

### `diff`

- Description: Compares two files line by line and displays the differences between them.

- Example usage:

  ```bash
    diff file1.txt file2.txt # Compares contents of file1.txt and file2.txt and displays differences
  ``` -->

---

### `less`

- Description: Allows scrolling through the contents of a file.

- Example usage:

  ````bash
  less book.txt # Opens 'book.txt' for browsing its content
  ```
  ````

**Note**: `more` and `less` are both used to view file contents in a terminal. However, less is an improved version of more.

<!-- ### ``

- Description:

- Example usage:

  ````bash

  ```
  ```` -->

<!-- to-do
- add tree command
- more details on diff command and how to read its output
- -->
