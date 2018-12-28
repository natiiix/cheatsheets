# Bash

Always remember to wrap all file names in quotes (especially when using variables, command line arguments and function parameters) to avoid problems caused by unexpected whitespace characters.

## Shebang

This should be the first line of code in any bash script.

```bash
#!/bin/bash
```

## Fail at first error

If you want the script to fail as soon as an error occurs, place this line before any other code.

```bash
set -e
```

## Function definition

Function parameters are accessed the exact same way as command line arguments (using `$1`, `$2`, etc.).

```bash
function FunctionName {
    # Code To Execute
}
```

## `find` command

### `-name`

**Filter by file name literal**

`*` works as placeholder for any number of any characters.

**Example:** `-name "*.cpp"` - All files with the extension `.cpp`

---

### `-regex`

**Filter by file name regex**

**Warning:** The regex must match the full file name and many special characters must be escaped

**Example:** `-regex '.*\(\.mkv\|\.mp4\|\.avi\)'` - All files with an extension `.mkv`, `.mp4` or `.avi`

---

### `-iname` and `-iregex`

**Case-insensitive versions of `-name` and `-regex` respectively**

---

### `-type`

**Filder by file type** (`f` for file, `d` for directory, etc.)

**Example:** `-type f` - Only regular files

---

### `-exec`

**Execute the specified command for each found file**

`{}` works as a placeholder for the name of the file in the command.

Command must be terminated with `\;`.

**Example:** `-exec cat "{}" \;` - Execute the `cat` command on each found file
