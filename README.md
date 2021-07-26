check_zfs
=========

This is a simple Nagios plugin to check the status of ZFS zpools on a
system.

It checks the following things:

 * pool, vdev, and disk state - problems are reported if state is
   anything other than "ONLINE"
 * read, write, and checksum error counts - problems are reported if
   the counts are greater than zero
 * pool usage - problems are reported if used pool capacity exceeds
   given thresholds


Installation
------------

Just copy the `check_zfs` program somewhere and configure Nagios (or
NRPE) to run it.  The `zpool` program must be in the `$PATH`, and the
user running `check_zfs` must have permissions to run `zpool status`
and `zpool list`.

Python 3 must be installed.  The program should work with Python
version 3.4 or any later version.


License
-------

To the extent possible under law, the author(s) have waived all
copyright and related or neighboring rights to this work under the
terms of the [CC0 1.0 Universal Public Domain Dedication][CC0].

  [CC0]: https://creativecommons.org/publicdomain/zero/1.0/
