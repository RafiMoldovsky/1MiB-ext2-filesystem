# Hey! I'm Filing Here

This code creates a 1MiB ext2 filesystem with 2 directories, 1 file, and 1 symbolic link.
## Building

To build the program type "make" in the correct repository.

## Running

To create the .img, run "./ext2-create". To mount it to a directory, first create the directory (or use an already created one) with "mkdir" then mnt the filesystem, type "sudo mount -o loop cs111-base.img YOURDIRHERE". 
Example of ls -ain of mounted filesystem:
ls -ain mnt 
total 7
     2 drwxr-xr-x 3    0    0 1024 Aug 25 12:10 .
141042 drwxr-xr-x 3 1000 1000 4096 Aug 25 12:11 ..
    13 lrw-r--r-- 1 1000 1000   11 Aug 25 12:10 hello -> 'hello world'
    12 -rw-r--r-- 1 1000 1000   12 Aug 25 12:10 hello-world
    11 drwxr-xr-x 2    0    0 1024 Aug 25 12:10 lost+found


## Cleaning up

To unmount the filesystem: "sudo umount YOURDIRHERE" 
To remove the directory: "rmdir YOURDIRHERE"
Then type "make clean" to clean up all binary files.

