# stash

`stash` is a command line utility for working with files across folders. It lets you save
(or stash) files across many folders and copy or move them to new locations.

# Usage

`stash [command (optional)]`

If command is omitted the command `stash` is assumed.

## Commands

 * **`stash [file]`:** Save given file at the top of the stash
 * **`pop`:** Print the file at the top of the stash. Remove it from the stash.
 * **`cp [directory (optional)]`:** Copy the file at the top of the stash to given target dir. Remove it from the stash. If target dir is omitted, current directory is assumed.
 * **`mv [target]`:** Move the file at the top of the stash to given target dir. Remove it from the stash. If target dir is omitted, current directory is assumed.
 * **`ls`:** List all files in the stash, in reverse insertion order.

# Examples

Move `file1` from `~/foo` to `~/bar`.

```bash
cd ~/foo
stash file1
cd ..
cd bar
stash mv
```

Move `file1` and `file2` from `~/foo` to `~/bar`.

```bash
cd ~/foo
stash file1
stash file2
cd ..
cd bar
stash mv
stash mv
```
