# Answer 1

`/mnt/c/Windows/system32`

# Answer 2

`ls -a` shows the **hidden files and folders** too, which plain `ls` does not.

# Answer 3

The first column, `drwxr-xr-x`, tells you what the file is and who is allowed to use it.

- The **`d`** means that it is a **directory**, not a regular file.
- The first **`rwx`** means I can **read, write, and access/open the folder**.
- The second **`r-x`** means anyone in my **group can read/access it but cannot change anything**.
- The last **`r-x`** means everyone else can **read/access it but cannot modify it**.
# Answer 4

It works because `coding-cafe/week02` is a **relative path** — it's relative to my current location. Since I'm standing in my home folder and `coding-cafe` is inside it, the shell just walks down from there without needing the full path from `/`.
# Answer 5

`mv` did two different jobs here. First, `mv README-backup.md week01/` moved the file into a different folder — same name, new location. Then `mv README-backup.md old-readme.md` renamed it — same location, new name. `mv` doesn't really tell the difference between moving and renaming; it just depends on whether you give it a new folder or a new filename.
# Answer 6

There are **23 folders**.

# Answer 7

`python3` lives at `/usr/bin/python3`.

# Answer 8

My `python3` path (`/usr/bin/python3`) was the same as my partner's. That makes sense since we're both using WSL with a similar Ubuntu setup, so `python3` comes from the same system package in the same default location.

# Answer 9

The shell said `Command 'pyton3' not found`, as there is no command saved as `pyton3`. It also suggested the actual `python3`.

This shows that it is smart enough to suggest me the **closest option**.

# Answer 10

`.venv` starts with a dot, which makes it a **hidden file/folder** in Linux — plain `ls` skips anything starting with `.` by default.

That's the same behavior we saw back in Section 1: `ls -a` shows **"all"** files, including hidden ones, while plain `ls` hides them to keep clutter (like config files) out of normal listings.

# Answer 11

After activating, `(.venv)` appeared at the very start of my prompt, before my username. It's a visual reminder that I'm currently **"inside" the virtual environment**, so any Python or pip commands I run will use the versions installed in `.venv` rather than the system-wide ones.

# Answer 12

No, it's different. Before activating, `python3` pointed to `/usr/bin/python3`. Now it points to `/home/gcp7r/coding-cafe/.venv/bin/python3`.

This tells me that `activate` doesn't magically know to use the venv's Python — it just quietly adds the venv's `bin` folder to the **front** of my `PATH`.

Since the shell searches `PATH` in order and stops at the first match, it now finds the venv's `python3` before it ever gets to `/usr/bin`.

# Answer 13

The first `pip list` only showed `pip` itself — a totally clean environment. After installing `requests`, the second list shows five new packages: `requests` itself, plus its four dependencies (`certifi`, `charset-normalizer`, `idna`, `urllib3`) that got pulled in automatically to make `requests` work.

# Answer 14

Back to `/usr/bin/python3` — the system-wide Python. `deactivate` removes the venv's `bin` folder from the front of `PATH`, so the shell goes back to finding the regular system Python first, same as before I ever activated the venv.

# Answer 15

`-h` makes file sizes shown by `ls -l` **"human-readable."** Instead of showing raw byte counts like `4096`, it shows sizes like `4.0K` or `1.2M`, which are much easier to scan quickly.

# Answer 16

Ctrl+C interrupted what was running but kept me inside the Python prompt — it just cancels the current action.

Ctrl+D, on the other hand, actually closed Python and sent me back to my normal terminal, because it signals **"end of input,"** telling the program there's nothing more coming, so it should exit.
