[Back to Start](../../README.md)

# Mount Disk Partition

**List information about block devices**

1. Run commando to list block devices

`lsblk`

2. Check if there is and sdb partition with available space

3. Run
`mount /dev/{partition_that_must_be_mount} /mnt/path`