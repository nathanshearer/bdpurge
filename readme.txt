Description:
  Erase a block device

Usage:
  bdpurge [options] BLOCK_DEVICE

Options:
  -h, --help
    Display this help message and exit.
  -n N
    Sets the niceness to N (default 0).
  -p, --pretend
    Performs a dry run and prints out what purge commands would be performed.
    Data is not actually purged.
  -r, --recursive
    Purge each partition before purging the entire block device.
  -s, --size 16777216
    The amount of data to erase at both ends of the block device.

Examples:
  bdpurge -r -p /dev/disk/by-id/ata-ST8000AS0002-1NA17Z_00000000

Version:
  bdpurge 1.0.1.0
  Copyright (C) 2016 Nathan Shearer
  Licensed under GNU General Public License 2.0
