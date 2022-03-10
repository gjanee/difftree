# difftree

`difftree` compares two directory trees.  Use this script to, for
example, compare a filesystem to a backup.  The output is similar to
that produced by `diff -qr`, but `difftree` also compares file
attributes (permissions, etc.) and is more intelligent about symbolic
links (it does not follow symbolic links, but compares the links
themselves).

File attributes that are NOT compared: device number; inode number;
number of hard links; number of blocks; last access time; last status
change time; and non-POSIX attributes.  Permissions and modification
times of symbolic links are not compared because these attributes are
typically not preserved by copy or backup tools.

Included in this repository is a companion script, `difftree-touch`,
that triggers MacOS Time Machine to back up files that are
persistently not being backed up.

Both scripts contain detailed usage information.
