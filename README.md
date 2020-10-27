# backupScript

backup.py

Create an archive which will be suitable for rsyncing to a remote backup.
 - will not copy data unnecessarily for common operations such as
   renaming a file or reorganising the directory structure.
   (assumes large files are generally going to be immutable, e.g. audio/video)
 - doesn't try to do anything fancy with permissions etc. Just a simple copy of each file.
Usage:
 backup.py source-paths-file destination-path [exclude-patterns-file]
 source-directories-file should be a text file with paths to be backed up, one per line.
 
 exclude-patterns-file is an optional text file of (python) regular expressions
 used to exclude matching files from the backup.
"""
