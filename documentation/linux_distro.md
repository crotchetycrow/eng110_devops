# Linux - Ubuntu distro

- `sudo apt-get update` - Update
- `sudo apt-get upgrade` - Upgrade
- `sudo apt-get install` - Installs a package
- `systemctl status package_name` - Checks the status of the package
- `uname` - Who am I (which machine am I using)
  - `uname -a` - More detail on who I am
- `pwd` - Where am I
- `ls` - How to check files/folders in existing locations
  - `ls -a` - Hidden folders
- `mkdir directory_name` - Make a directory
- `cd folder_name` - Navigate to a folder
- `cd ..` - Change back to previous directory
  - `cd` - Change back to home location
- `touch` - Creates a file
  - `nano` - Creates and edits a file
- `cat` - Allows user to view contents of a file
- `cp location_file_name to destination_path` - Allows the user to copy a file from one location to another
- `mv file_name destination_path/renamed_file` - Allows the user to move file to a new location and rename the file (optional)
- `rm file or folder_name` - Deletes file/folder
  - `rm -rf file or folder_name` - Force delete
- `top` - Check running processes (ctrl + c to exit)
  - `ps aux` - More detailed `top`
- `kill pid` - End task/process

## Permissions

- `ll` - Checks permissions
- `sudo su` - Switch to `root user`
  - `root user` is not best practice as it doesn't double check permissions
- `chmod permission file_name` - Change file permissions

  - `+` = ADD
  - `-` = REMOVE
  - `=` = SETS/OVERRIDES EARLIER PERMISSIONS

---

- `r` = read permissions
- `w` = write permissions
- `x` = execute permissions
- `-` = no permissions

---

- `0` = No permissions
- `1` = Execute permissions
- `2` = Write permissions
- `3` = Execute + write permissions
- `4` = Read permissions
- `5` = Read + execute permissions
- `6` = Read + write permissions
- `7` = Read + write + execute permissions

---

- Absolute numeric mode example `400`
  - First number is owner permissions
  - Second number is usergroup permissions
  - Third number is world permissions

---

## Processes

- `fg` - Job control, allows processes to run in the foreground

- `bg` - Job control, allows processes to run in the background
- `CTRL-Z` - Stops the foreground process and places it in the background as a stopped process
- `wait` - Job control, suspends script execution until all jobs running in background have terminated

  - `wait job_identifier - wait%1` - optional job identifier argument

- Running in background example: `sleep 100 &`
  - process command &
- `jobs` - Shows currently running jobs
- `kill` - Destroys program

---

## Sending data from host to VM

- `config.vm.provision "file", source: "~/.gitconfig", destination: ".gitconfig"` - This is for files. Placed in Vagrantfile (creates location if it doesn't exist)
- `config.vm.synced_folder "/src_folder", "/vm_location"` - This is for folders. Placed in Vagrantfile (creates location if it doesn't exist)
