# Remove log file rotations

This script removes compressed files and related kinds of archive files.

This searches by file name extension:

  * .bz, .bz2, .bzip, .gz, .tar, .tgz, .zip, .7zip.

Syntax:

    rm-compressed-files [dir]

Example to do the current directory:

    rm-compressed-files

Example to do a specific directory:

    rm-compressed-files /foo/goo

This searches by file name extension:

  * .bz, .bz2, .bzip, .gz, .tar, .tgz, .zip, .7zip.

Compatibility notes:

  * We prefer to be more compatible rather than system-specific.

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

Tracking:

  * Command: rm-compressed-files
  * Version: 2.0.0
  * Created: 2013-12-09
  * Updated: 2017-08-29
  * License: GPL
  * Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)

