---
title: "Linux Find Command"
date: 2023-09-17T21:21:30+01:00
draft: false
tags: ["Linux"]
author: "Me"
hidemeta: false
comments: false
canonicalURL: "https://linuxdojo.co.uk/docs/find"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/andrewglass3/doc"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

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
