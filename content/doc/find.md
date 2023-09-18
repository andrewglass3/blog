+++
title = 'Linux Find Command'
date = 2023-09-17T21:21:30+01:00
draft = false
+++

# Find and remove - A quick note and Warning

```
find . -name '.git' -type d -prune -exec rm -rf '{}' \;
```

Here's what it does:

- **`find .`** searches the current directory and its subdirectories.
- **`name '.git'`** matches files and directories named .git.
- **`type d`** makes the command only consider directories (since .git is a directory).
- **`prune`** prevents **`find`** from descending into the current file if it is a directory, which helps when you're wanting to remove the directory itself.
- **`exec rm -rf '{}' \;`** removes the matched directories, and all of their contents.

Please remember, as mentioned before, you need to be very careful with recursive removes. Always make sure you are in the correct directory before executing this command, and ideally, have a backup of your files.
