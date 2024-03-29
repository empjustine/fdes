# fdes (File Description)

A command line utility for adding a description to files.

## Configuration

The 'db' path in /.config/fdes/fdesrc is a file path for an sqlite3 database. If it does not exist, it will be created at this path during the first run.
The default database path is ~/.local/share/fdes/.fdes.db

## Installation

Requires Python3

```bash
git clone https://github.com/jmh2012/fdes.git
cd fdes
python3 setup.py install --user  # Install locally
```

## Usage Examples

```bash
# Add a description to a file
$ fdes set -f <filename>

# Get the description of a file
$ fdes get -f <filename>

# Copy the description of one file to another.
$ fdes copy -f <filename> -d <new filename destination>

# List all file descriptions set by your user
$ fdes listall
+-------------+-------------------------------------+
|  File Name  |             Description             |
+-------------+-------------------------------------+
| /etc/passwd |      This is the password file.     |
|     /etc    | This directory is for config files. |
|     /bin    |  This directory is for executables. |
+-------------+-------------------------------------+

# Remove a description for a file
$ fdes remove -f <filename>

# Remove all descriptions for files under a directory (including directory itself)
$ fdes removedir -f <directory>

# Clean up database of any files that don't exist anymore
$ fdes cleanup
Removed description for deleted file /home/user/oldfile
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)
