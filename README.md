# Remove compressed files

This script removes compressed files and related kinds of archive files.

Contents:

* [Introduction](#introduction)
* [Which files?](#which-files)
* [Related](#related)
* [Compatibility notes](#compatibility-notes)
* [Tracking](#tracking)


## Introduction

Syntax:

    $ rm-compressed-files [dir]

Example to do the current directory:

    $ rm-compressed-files

Example to do a specific directory:

    $ rm-compressed-files /foo/goo

This searches by file name extension:

  * .bz, .bz2, .bzip, .gz, .tar, .tgz, .zip, .7zip.


## Which files?

This searches by file name extension:

  * .bz, .bz2, .bzip

  * .gz, .tgz

  * .tar, .tar.xy, .tar.lz

  * .zip, .7zip


## Related

These scripts are for related purposes:

  * [rm-compressed-files](https://github.com/SixArm/rm-compressed-files)

  * [rm-dated-files](https://github.com/SixArm/rm-dated-files)
  
  * [rm-numbered-files](https://github.com/SixArm/rm-numbered-files)
  
  * [rm-rotated-files](https://github.com/SixArm/rm-rotated-files)


## Compatibility notes

We prefer to be more compatible rather than system-specific.

  * To delete files, we prefer `-exec rm` vs. `-delete`.
    The former is more compatible, the latter is faster.

  * To name match, we prefer using `-name` vs. `-iname`.
    This means we need to match on upper case and lower case.

  * To regex match, we prefer patterns to be basic vs. extended.
    The former is more compatible, the latter is more modern.

  * We prefer POSIX code vs. shell-specific code.

  * We prefer the code to be more DAMP than DRY.
    For example, the code has separate name matching 
    for `.bz` and `.bz2`, even though we could combine these.


## Tracking

  * Command: rm-compressed-files
  * Website: http://sixarm.com/rm-compressed-files
  * Cloning: https://github.com/sixarm/rm-compressed-files
  * Version: 4.1.0
  * Created: 2013-12-09
  * Updated: 2019-01-04
  * License: GPL
  * Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)
  * Tracker: 9c5b1940fec3ac49b828a9a8d2d2014b
