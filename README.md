# MakeMKV Renamer

This is a simple utility to rename the output of MakeMKV when ripping TV shows.

#### Help

```
makemkv-renamer$ ./renamer -h
usage: renamer [-h] --output OUTPUT [--prefix PREFIX] [--offset OFFSET]
               [--start START] [--dir DIR] [--extension EXTENSION]

Rename the output from MakeMKV. (C) 2015 Andrew Scagnelli

optional arguments:
  -h, --help            show this help message and exit
  --output OUTPUT       The output prefix
  --prefix PREFIX       The input prefix to change (eg title in title00.mkv)
  --offset OFFSET       The offset between the input and output files.
  --start START         The value to start counting from.
  --dir DIR             The directory to loop through.
  --extension EXTENSION
                        File extension to monitor.

(C) 2015 Andrew Scagnelli. Available under the GNU GPL.
```

#### Sample Invocation/output

```
makemkv-renamer$ ls -l
total 48
-rw-r--r--  1 ascagnel  staff   847 Jul 12 15:16 README.md
-rwxr-xr-x  1 ascagnel  staff  2566 Jul 12 15:15 renamer
-rw-r--r--  1 ascagnel  staff     0 Jul 12 15:18 title00.mkv
-rw-r--r--  1 ascagnel  staff     0 Jul 12 15:18 title01.mkv
-rw-r--r--  1 ascagnel  staff     0 Jul 12 15:18 title02.mkv
-rw-r--r--  1 ascagnel  staff     0 Jul 12 15:18 title03.mkv
-rw-r--r--  1 ascagnel  staff     0 Jul 12 15:18 title04.mkv
makemkv-renamer$
makemkv-renamer$ ./renamer --output "Show Name - S01E"
Pre-check passed
Renaming title00.mkv to Show Name - S01E01.mkv
Renaming title01.mkv to Show Name - S01E02.mkv
Renaming title02.mkv to Show Name - S01E03.mkv
Renaming title03.mkv to Show Name - S01E04.mkv
Renaming title04.mkv to Show Name - S01E05.mkv
makemkv-renamer$
makemkv-renamer$ ls -l
total 48
-rw-r--r--  1 ascagnel  staff   847 Jul 12 15:16 README.md
-rw-r--r--  1 ascagnel  staff     0 Jul 12 15:18 Show Name - S01E01.mkv
-rw-r--r--  1 ascagnel  staff     0 Jul 12 15:18 Show Name - S01E02.mkv
-rw-r--r--  1 ascagnel  staff     0 Jul 12 15:18 Show Name - S01E03.mkv
-rw-r--r--  1 ascagnel  staff     0 Jul 12 15:18 Show Name - S01E04.mkv
-rw-r--r--  1 ascagnel  staff     0 Jul 12 15:18 Show Name - S01E05.mkv
-rwxr-xr-x  1 ascagnel  staff  2566 Jul 12 15:15 renamer
```