Let's do some practical stuff with filesytems by working through the process on a USB drive. If you don't have one, no worries, you can still follow along these next couple of lessons. 

First we'll need to partition our disk. There are many tools available to do this: 

* `fdisk` - basic command-line partitioning tool, it does not support GPT
* `parted` - this is a command line tool that supports both MBR and GPT partitioning
* `gparted` - this is the GUI version of parted
* `gdisk` - fdisk, but it does not support MBR only GPT

Let's use parted to do our partitioning. Let's say I connect the USB device and we see the device name is /dev/vdb2. 

**Launch parted**

```
$ sudo parted
```

You'll be entered in the parted tool, here you can run commands to partition your device. 

**Select the device**

```
select /dev/vdb
```

To select the device you'll be working with, select it by its device name.

**View current partition table**

```

(parted) print                                                            
Model: Seagate (scsi)
Disk /dev/sda: 21.5GB
Sector size (logical/physical): 512B/512B
Partition Table: msdos

Number  Start   End     Size    Type      File system     Flags
 1      1049kB  6860MB  6859MB  primary   ext4            boot
 2      6861MB  21.5GB  14.6GB  extended
 5      6861MB  7380MB  519MB   logical   linux-swap(v1)
 6      7381MB  21.5GB  14.1GB  logical   xfs

```

Here you will see the available partitions on the device. The **start** and **end** points are where the partitions take up space on the hard drive, you'll want to find a good start and end location for your partitions. 

If you experience an error, go back and complete step 3.

**Partition the device**

```
mkpart primary 123 4567
```

Now just choose a start and end point and make the partition, you'll need to specify the type of partition depending on what table you used. 

Now, create an extended partition:

```
mkpart extended 4600 6000
```
 and within the start and end points of that partition, create a logical partition.

```
mkpart logical 4700 5000
```

View the partions on the device with

```
(parted) print
```
**Resize a partition**

You can also resize a partition if you don't have any space. 

```
(parted) resizepart
Partition number? 2
End? [6000MB]? 6200
```

Select the partition number and then the start and end points of where you want to resize it to. 

Parted is a very powerful tool and you should be careful when partitioning your disks. 

## Exercise

Partition a USB drive with half of the drive as ext4 and the other half as free space. 

>>Q1: What is the `parted` (sub)command to make a partition?<<
=== mkpart
