(Core AWS storage services, AWS course)
***
# Primary storage types

![[Pasted image 20221217184659.png]]
***

## Block storage

Block storage is a raw storage which based on a hardware storage device or volume, formatted and attached to the compute system for use. The storage is formatted in predefined continuous segments, they are called blocks. Blocks are basic fixed storage units used to store data on the device.

Storage device can be HDD, SSD or NVMe. In addition to individual storage devices, you can deploy block storage on SAN (Storage Area Network) systems.

![[Pasted image 20221217190121.png]]
***

## File storage

File storage is build on top of block storage, typically serving as a file or share server.
It is created using the operating system that formats and manages the reading and writing of data to the block storage devices. The name "file storage" comes from the primary use of storing data as files, typically in a directory tree hierarchy.

The two most common storage protocols for the file storage are SMB (Server Message Block) and NFS (Network File System). You can use network protocols to communicate with remote computers and servers. You can use server resources to share, open and edit files.

The operating system manages the storage protocols to operate the file system.
You can use any available operating system such as Windows, Linux or specialized OS used on NAS (Network Attached Storage) devices or clustered NAS systems.

![[Pasted image 20221217191716.png]]
***

## Object storage

Object storage is also built on top of block storage. Object storage is created using an operating system that formats and manages block storage devices. The name "object storage" comes from the primary using use of storing the data within a binary object. Unlike file storage, object storage does not differentiate between types of data. The type of data or the file type becomes part of the data's metadata.

An object is made up of a larger set of blocks organized by using a predetermined size.
For example, one object storage system uses binary object sizes of 128 MB (megabytes).
Smaller files or data are stored on the binary level within the object. Larger data files are stored by spreading the data across multiple objects.

Object storage is recognized for its inherit availability of the file objects. Some systems support file versioning, tracking and retention.

![[Pasted image 20221217192743.png]]
***

# AWS storage services

![[Pasted image 20221217194025.png]]



