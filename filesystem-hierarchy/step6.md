Before you can view the contents of your filesystem, you will have to mount it. To do that I'll need the device location, the filesystem type and a mount point, the mount point is a directory on the system where the filesystem is going to be attached. So we basically want to mount our device to a mount point. 

First create the mount point; type

```
 $ mkdir /mydrive

```
and then

```
$ sudo mount -t ext4 /dev/vdb1 /mydrive
```

Simple as that! Now when we go to /mydrive we can see our filesystem contents, the **-t** specifies the type of filesystem, then we have the device location, then the mount point. 

To unmount a device from a mount point: 

```
$ sudo umount /mydrive
```

or 

```
$ sudo umount /dev/vdb1
```

Remember that the kernel names devices in the order it finds them. What if our device name changes for some reason after we mount it? Well fortunately, you can use a device's universally unique ID (UUID) instead of a name.

To view the UUIDS on your system for block devices:

```

$ sudo blkid
/dev/sda1: UUID="130b882f-7d79-436d-a096-1e594c92bb76" TYPE="ext4" 
/dev/sda5: UUID="22c3d34b-467e-467c-b44d-f03803c2c526" TYPE="swap" 
/dev/sda6: UUID="78d203a0-7c18-49bd-9e07-54f44cdb5726" TYPE="xfs" 

```

We can see our device names, their corresponding filesystem types and their UUIDs. Now when we want to mount something, we can use:

```
$ sudo mount UUID=130b882f-7d79-436d-a096-1e594c92bb76 /mydrive
```

Most of the time you won't need to mount devices via their UUIDs, it's much easier to use the device name and often times the operating system will know to mount common devices like USB drives. If you need to automatically mount a filesystem at startup though like if you added a secondary hard drive, you'll want to use the UUID and we'll go over that in the next lesson.

## Exercise

Look at the manpage for mount and umount and see what other options you can use.

>>Q1: What command is used to attach a filesystem?<<
=== mount
