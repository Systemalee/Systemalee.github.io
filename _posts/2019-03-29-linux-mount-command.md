---
layout: post
title: "Linux-Command-Mount"
date: 2019-03-29
excerpt: "this post explan that the Linux Command"
tags: [linux, mount]
feature: http://i.imgur.com/Ds6S7lJ.png
comments: true
---

### Linux Command 

mount

commnad : mount [option] [device] [directory]

###[OPTION]
-a :  Mount all the filesystems in "/ etc / fstab".
-c :  Specifies the file system. It is used with a file system name like "-t ext2".
-o : Other options can be specified.

####-t [file system]
msdos, vfat, ntfs, ext2, ext3, ext4, iso9660 ( CD/DVD )
nfs ( network file system )
udf ( DVD file system, iso9660 )

####-o [options]
ro : read only
remount
loop : iso file mount 
noatime : Option to not change access time until file is read
username= account, password = password 
acl : Access Control Lists mount option


###[DEVICE]
FDD: /dev/fd0
CD/DVD: /dev/cdrom, /dev/dvd
IDE HDD: dev/hda
USB, SCSI HDD, SATA HDD: /dev/sda, /sdb


###Example
mount -o port=2049,nolock,proto=tcp -t nfs 187.1.45.172:/home/ehdgns104/nfs/ /mnt/