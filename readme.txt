Description:
  Erase a block device

Usage:
  bdpurge [options] BLOCK_DEVICE

Options:
  -e, --email mail@example.com
    Send an email upon completion of the badblocks method.
  -f, --force
    Erase the block device even if it is mounted.
  -h, --help
    Display this help message and exit.
  -m, --method quickr
    Set the method used to erase the block device. Default is quickr:
      badblocks  Write 4 passes of 0xaa, 0x55, 0xff, and 0x00
      quick      Erase both ends of the device
      quickr     Erase both ends of each partition and the device
      trim       Erase the entire device with the trim command
      urandom    Write 1 pass with data from /dev/urandom
      zero       Write 1 pass with data from /dev/zero
  -n, --nice N
    Sets the niceness to N (default 0).
  -s, --size 16777216
    The amount of data to erase at both ends of the block device.

Examples:
  bdpurge -r -p /dev/disk/by-id/ata-ST8000AS0002-1NA17Z_00000000

Version:
  bdpurge 2.3.2.0
  Copyright (C) 2016 Nathan Shearer
  Licensed under GNU General Public License 2.0
