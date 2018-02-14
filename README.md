# Opencontig
Opencontig is a CLI Windows tool to defragment (and fragment) files and folders. It includes almost the whole functionality of the Sysinternals tool (contig.exe) but it's open source and distributable under the license conditions.
It's perfect for quickly optimizing files that are continuously becoming fragmented, or that you want to ensure are in as few fragments as possible.

## Features
* Analysis of free space fragmentation on a volume
* Fragmentation analysis of files and folders
* Defragmentation of files or folder
* Fragmentation of files or folder (yup, I know, but it can be funny and even useful in rare occasions)
* NTFS and FAT support
* Works on Windows XP, Windows Server 2003 and higher (including 64-bit versions).
## Usage
##### Analyzing the fragmentation of a folder
```
C:\>opencontig -analyze Folder

OpenContig v1.0 File defragmentation/fragmentation tool.
Copyright (c) 2013 

C:\Folder\IE10-Windows6.1-x64-es-es.exe is defragmented
C:\Folder\npp.6.6.9.Installer.exe is defragmented
C:\Folder\SubFolderA\GitHubSetup.exe is defragmented
C:\Folder\SubFolderA\VirtualBox-4.3.18-96516-Win.exe is defragmented
C:\Folder\SubFolderB\Git-1.9.4-preview20140929.exe is defragmented
C:\Folder\SubFolderB\VirtualBox-4.2.26-95022-Win.exe is defragmented
C:\Folder\SubFolderC\semantic.zip is defragmented
C:\Folder\SubFolderC\white_noise.msi is defragmented
C:\Folder\SubFolderD\IE11-Windows6.1.exe is defragmented
C:\Folder\SubFolderD\Windows6.1-KB2639308-x64.cab is defragmented

Number of files processed: 10
Average fragmentation:     1 frags/file
```
##### Ok, the folder is defragmented. Let's fragment it: 
```
C:\>opencontig.exe -fragment Folder

OpenContig v1.0 File defragmentation/fragmentation tool.
Copyright (c) 2013 

Processing C:\Folder\IE10-Windows6.1-x64-es-es.exe...
Processing C:\Folder\npp.6.6.9.Installer.exe...
Processing C:\Folder\SubFolderA\GitHubSetup.exe...
Processing C:\Folder\SubFolderA\VirtualBox-4.3.18-96516-Win.exe...
Processing C:\Folder\SubFolderB\Git-1.9.4-preview20140929.exe...
Processing C:\Folder\SubFolderB\VirtualBox-4.2.26-95022-Win.exe...
Processing C:\Folder\SubFolderC\semantic.zip...
Processing C:\Folder\SubFolderC\white_noise.msi...
Processing C:\Folder\SubFolderD\IE11-Windows6.1.exe...
Processing C:\Folder\SubFolderD\Windows6.1-KB2639308-x64.cab...

Number of files processed: 10
Average fragmentation before:     1 frags/file
Average fragmentation after:      7865.9 frags/file
```
##### That's what I call fragmentation. Let's analyze it:
```
C:\>opencontig.exe -analyze Folder

OpenContig v1.0 File defragmentation/fragmentation tool.
Copyright (c) 2013 

C:\Folder\IE10-Windows6.1-x64-es-es.exe is in 11329 fragments
C:\Folder\npp.6.6.9.Installer.exe is in 1940 fragments
C:\Folder\SubFolderA\GitHubSetup.exe is in 166 fragments
C:\Folder\SubFolderA\VirtualBox-4.3.18-96516-Win.exe is in 26683 fragments
C:\Folder\SubFolderB\Git-1.9.4-preview20140929.exe is in 4352 fragments
C:\Folder\SubFolderB\VirtualBox-4.2.26-95022-Win.exe is in 25864 fragments
C:\Folder\SubFolderC\semantic.zip is in 611 fragments
C:\Folder\SubFolderC\white_noise.msi is in 5948 fragments
C:\Folder\SubFolderD\IE11-Windows6.1.exe is in 508 fragments
C:\Folder\SubFolderD\Windows6.1-KB2639308-x64.cab is in 1258 fragments

Number of files processed: 10
Average fragmentation:     7865.9 frags/file
```
##### This folder needs a defragmenter!
```
C:\>opencontig.exe -defrag Folder

OpenContig v1.0 File defragmentation/fragmentation tool.
Copyright (c) 2013 

Processing C:\Folder\IE10-Windows6.1-x64-es-es.exe...
Processing C:\Folder\npp.6.6.9.Installer.exe...
Processing C:\Folder\SubFolderA\GitHubSetup.exe...
Processing C:\Folder\SubFolderA\VirtualBox-4.3.18-96516-Win.exe...
Processing C:\Folder\SubFolderB\Git-1.9.4-preview20140929.exe...
Processing C:\Folder\SubFolderB\VirtualBox-4.2.26-95022-Win.exe...
Processing C:\Folder\SubFolderC\semantic.zip...
Processing C:\Folder\SubFolderC\white_noise.msi...
Processing C:\Folder\SubFolderD\IE11-Windows6.1.exe...
Processing C:\Folder\SubFolderD\Windows6.1-KB2639308-x64.cab...

Number of files processed: 10
Average fragmentation before:     7865.9 frags/file
Average fragmentation after:      1 frags/file
```
## License
opencontig is licensed under the Apache License, Version 2.0.
