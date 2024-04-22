# zv – z for vim

`zv` is like `z`, but for vim (or any other command).
It allows you to quickly open a file as long as it's been opened before with `vim`[^1] (since it's based on the `viminfo` file).

This has been inspired by [`rupa/v`](https://github.com/rupa/v), whose development seems to have stalled.
Differences can be found in the [What's changed?](#whats-changed) section.

## What's changed?

- `zv` is POSIX compliant and conformant to the [Utility Syntax Guidelines](https://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap12.html#tag_12_02), which means that it can be used without additional software in POSIX systems that don't have `bash` as their default shell, such as FreeBSD;
- `zv` can open files with any command, not just `vim` — the command can be specified with the `-c` option or the `ZV_CMD` environment variable;[^2]
- the default command is read from the `EDITOR` environment variable and can be overridden with the `ZV_CMD` environment variable;
- `ZV_VIMINFO` can be used to customize the path to the `viminfo` file.
- options are different, see the manual page for details.

[^1]: Or any other command, see [What's changed?](#whats-changed).
[^2]: Additional arguments may be specified here, e.g., `ZV_CMD='bat --style=full'`.

## Installation

Put `zv` somewhere in your `PATH` (e.g. `/usr/local/bin/`).

For the manual page, put `zv.1` somewhere in your `MANPATH` (e.g., `/usr/local/man/man1/`).
