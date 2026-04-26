# phptest

A lightweight Zsh command-line helper for recursively checking PHP files for syntax errors.

`phptest` scans a target directory for `.php` files, skips common dependency folders, runs `php -l` against each file, and prints a clear pass/fail result.

## Why I Built This

I originally used this as part of my WordPress security plugin workflow. Instead of manually checking individual PHP files after edits, I wanted a quick command that could scan the whole project and confirm that every PHP file still passed a syntax check.

## Features

- Recursively checks PHP files
- Skips `vendor` and `node_modules`
- Prints clear `PASS` and `FAIL` results
- Returns a non-zero exit code if any file fails
- Works well before committing PHP changes

## Usage

Check the current directory:

```zsh
./phptest