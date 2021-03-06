# Zaloha.sh

Zaloha is a shellscript for synchronization of files and directories. It is a much simpler alternative to RSYNC, with key differences:

 * Zaloha is a bash shellscript that uses only FIND, SORT and AWK.
 * All you need is the Zaloha.sh file (contains ~69 kB of program code and ~57 kB of documentation).
 * No compilation, installation and configuration is required.
 * Cyber-secure: No new binary code, no new open ports, easily reviewable.
 * Both directories must be available locally (local HDD/SSD, flash drive, mounted Samba or NFS volume).
 * Zaloha does not lock files while copying them. No writing on either directory may occur while Zaloha runs.
 * Zaloha always copies whole files (not parts of files like RSYNC). This is, however, fully sufficient in many situations.
 * Zaloha has optional reverse-synchronization features.
 * Zaloha can optionally compare files byte by byte.
 * Zaloha prepares scripts for case of eventual restore.

Full documentation is available both [online](DOCUMENTATION.md) as well as inside of Zaloha.sh.

On Linux/Unics, Zaloha runs natively. On Windows, Cygwin is needed.

## Usage Example

```bash
Zaloha.sh --sourceDir="test_source" --backupDir="test_backup" [other options, see docu]
```

## Usage Screenshot
![Simple_Demo_screenshot](Simple_Demo_screenshot.png)

## Add-on shellscript Zaloha_Snapshot.sh

An add-on shellscript to create hardlink-based snapshots of the backup directory exists: [Zaloha_Snapshot](https://github.com/Fitus/Zaloha_Snapshot.sh).
This allows to create **Time Machine**-like backup solutions.

## License
MIT License
