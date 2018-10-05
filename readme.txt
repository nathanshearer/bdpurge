Description:
  Erase a block device

Usage:
  bdpurge [options] BLOCK_DEVICE

Options:
  -f, --force
    Erase the block device even if it is mounted.
  -h, --help
    Display this help message and exit.
  -m, --method quick
    Set the method used to erase the block device. Default is quick:
      quick      Erase both ends of the device
      quickr     Erase both ends of each partition and the device
  -n N
    Sets the niceness to N (default 0).
  -p, --pretend
    Performs a dry run and prints out what purge commands would be performed.
    Data is not actually purged.
  -s, --size 16777216
    The amount of data to erase at both ends of the block device.

Examples:
  bdpurge -r -p /dev/disk/by-id/ata-ST8000AS0002-1NA17Z_00000000

Version:
  bdpurge 2.0.0.0
  Copyright (C) 2016 Nathan Shearer
  Licensed under GNU General Public License 2.0
