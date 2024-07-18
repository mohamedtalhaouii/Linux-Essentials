## Essential Linux Commands and Shell Scripting Guide

### Basic Commands

1. **`pwd`**: Print working directory.
   ```bash
   pwd
   ```
   - Displays the current working directory.

2. **`ls`**: List directory contents.
   ```bash
   ls
   ls -l  # Long listing format
   ls -a  # Show hidden files
   ```
   - Lists files and directories in the current directory.

3. **`cd`**: Change directory.
   ```bash
   cd /path/to/directory
   cd ..  # Move up one directory
   cd ~   # Move to the home directory
   ```
   - Changes the current directory.

4. **`mkdir`**: Make directories.
   ```bash
   mkdir new_directory
   mkdir -p /path/to/new_directory  # Create parent directories as needed
   ```
   - Creates new directories.

5. **`rmdir`**: Remove empty directories.
   ```bash
   rmdir empty_directory
   ```
   - Removes empty directories.

6. **`touch`**: Create an empty file or update a file's timestamp.
   ```bash
   touch newfile.txt
   ```
   - Creates or updates a file's timestamp.

7. **`rm`**: Remove files or directories.
   ```bash
   rm file.txt
   rm -r directory  # Recursively remove a directory
   ```
   - Removes files or directories.

8. **`cp`**: Copy files or directories.
   ```bash
   cp source.txt destination.txt
   cp -r source_directory destination_directory  # Recursively copy a directory
   ```
   - Copies files or directories.

9. **`mv`**: Move or rename files or directories.
   ```bash
   mv oldname.txt newname.txt
   mv file.txt /new/path/
   ```
   - Moves or renames files or directories.

10. **`cat`**: Concatenate and display file content.
    ```bash
    cat file.txt
    ```
    - Displays file content.

11. **`echo`**: Display a line of text.
    ```bash
    echo "Hello, World!"
    ```
    - Prints text to the terminal.

### File Permissions

1. **`chmod`**: Change file mode (permissions).
   ```bash
   chmod 755 file.txt  # rwxr-xr-x
   chmod u+x script.sh  # Add execute permission to the user
   ```
   - Changes file permissions.

2. **`chown`**: Change file owner and group.
   ```bash
   chown user:group file.txt
   ```
   - Changes file owner and group.

3. **`chgrp`**: Change group ownership.
   ```bash
   chgrp group file.txt
   ```
   - Changes group ownership.

### Process Management

1. **`ps`**: Report a snapshot of current processes.
   ```bash
   ps aux
   ```
   - Shows active processes.

2. **`top`**: Display Linux tasks.
   ```bash
   top
   ```
   - Displays system tasks.

3. **`kill`**: Send a signal to a process.
   ```bash
   kill PID
   kill -9 PID  # Forcefully kill a process
   ```
   - Terminates a process.

4. **`killall`**: Kill processes by name.
   ```bash
   killall process_name
   ```
   - Terminates processes by name.

5. **`bg`**: Resume a stopped job in the background.
   ```bash
   bg %1
   ```
   - Resumes a job in the background.

6. **`fg`**: Bring a job to the foreground.
   ```bash
   fg %1
   ```
   - Brings a job to the foreground.

7. **`jobs`**: List active jobs.
   ```bash
   jobs
   ```
   - Lists background jobs.

### File Searching

1. **`find`**: Search for files in a directory hierarchy.
   ```bash
   find /path/to/search -name "filename"
   ```
   - Searches for files.

2. **`grep`**: Print lines that match patterns.
   ```bash
   grep "pattern" file.txt
   grep -r "pattern" /path/to/search  # Recursive search
   ```
   - Searches for patterns in files.

3. **`locate`**: Find files by name.
   ```bash
   locate filename
   ```
   - Quickly finds files.

4. **`which`**: Locate a command.
   ```bash
   which command
   ```
   - Shows the path of a command.

### Disk Usage

1. **`df`**: Report file system disk space usage.
   ```bash
   df -h
   ```
   - Displays disk usage.

2. **`du`**: Estimate file space usage.
   ```bash
   du -sh /path/to/directory
   ```
   - Shows directory disk usage.

3. **`mount`**: Mount a file system.
   ```bash
   sudo mount /dev/sdX /mnt
   ```
   - Mounts a file system.

4. **`umount`**: Unmount file systems.
   ```bash
   sudo umount /mnt
   ```
   - Unmounts a file system.

### Networking

1. **`ping`**: Send ICMP ECHO_REQUEST to network hosts.
   ```bash
   ping example.com
   ```
   - Tests network connectivity.

2. **`ifconfig`**: Configure a network interface.
   ```bash
   ifconfig
   ```
   - Configures network interfaces.

3. **`netstat`**: Print network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.
   ```bash
   netstat -tuln
   ```
   - Shows network connections.

4. **`ssh`**: OpenSSH SSH client (remote login program).
   ```bash
   ssh user@host
   ```
   - Connects to a remote host.

5. **`scp`**: Secure copy (remote file copy program).
   ```bash
   scp file.txt user@host:/path/to/destination
   ```
   - Copies files between hosts.

6. **`wget`**: Non-interactive network downloader.
   ```bash
   wget http://example.com/file.zip
   ```
   - Downloads files from the web.

7. **`curl`**: Transfer data from or to a server.
   ```bash
   curl http://example.com
   ```
   - Transfers data via URLs.

### Package Management

1. **`apt-get`**: APT package handling utility (Debian-based).
   ```bash
   sudo apt-get update
   sudo apt-get install package_name
   ```
   - Manages packages on Debian-based systems.

2. **`yum`**: Package manager (RPM-based).
   ```bash
   sudo yum update
   sudo yum install package_name
   ```
   - Manages packages on RPM-based systems.

3. **`dpkg`**: Debian package manager.
   ```bash
   sudo dpkg -i package.deb
   ```
   - Manages Debian packages.

4. **`rpm`**: RPM package manager.
   ```bash
   sudo rpm -i package.rpm
   ```
   - Manages RPM packages.

### Compression

1. **`tar`**: Archive files.
   ```bash
   tar -cvf archive.tar directory
   tar -xvf archive.tar
   ```
   - Creates and extracts tar archives.

2. **`gzip`**: Compress files.
   ```bash
   gzip file.txt
   ```
   - Compresses files.

3. **`gunzip`**: Decompress files.
   ```bash
   gunzip file.txt.gz
   ```
   - Decompresses gzip files.

4. **`zip`**: Package and compress files.
   ```bash
   zip archive.zip file.txt
   ```
   - Creates zip archives.

5. **`unzip`**: Extract compressed files.
   ```bash
   unzip archive.zip
   ```
   - Extracts zip archives.

### Text Processing

1. **`awk`**: Pattern scanning and processing language.
   ```bash
   awk '{print $1}' file.txt
   ```
   - Processes text based on patterns.

2. **`sed`**: Stream editor for filtering and transforming text.
   ```bash
   sed 's/old/new/g' file.txt
   ```
   - Edits text in streams.

3. **`sort`**: Sort lines of text files.
   ```bash
   sort file.txt
   ```
   - Sorts lines in text files.

4. **`uniq`**: Report or omit repeated lines.
   ```bash
   uniq file.txt
   ```
   - Filters out repeated lines.

### System Information

1. **`uname`**: Print system information.
   ```bash
   uname -a
   ```
   - Displays system information.

2. **`uptime`**: Tell how long the system has been running.
   ```bash
   uptime
   ```
   - Shows system uptime.

3. **`dmesg`**: Print or control the kernel ring buffer.
   ```bash
   dmesg
   ```
   - Prints kernel messages.

4. **`who`**: Show who is logged on.
   ```bash
   who
   ```
   - Displays logged-in users.

5. **`free`**: Display the amount of free and used memory in the system.
   ```bash
   free -h
   ```
   - Shows memory usage.

### User Management

1. **`adduser`**: Add a user

 to the system.
   ```bash
   sudo adduser username
   ```
   - Adds a new user.

2. **`deluser`**: Remove a user from the system.
   ```bash
   sudo deluser username
   ```
   - Removes a user.

3. **`passwd`**: Update a user’s authentication tokens (password).
   ```bash
   passwd
   ```
   - Changes a user's password.

### Shell Scripting

#### Writing a Shell Script

1. **Create a new file**: 
   ```bash
   touch script.sh
   ```
   - Creates a new script file.

2. **Make it executable**:
   ```bash
   chmod +x script.sh
   ```
   - Makes the script executable.

3. **Edit the script**:
   ```bash
   nano script.sh
   ```
   - Opens the script in a text editor (e.g., nano).

4. **Sample Script**:
   ```bash
   #!/bin/bash
   echo "Hello, World!"
   ```
   - A simple script that prints "Hello, World!".

5. **Run the script**:
   ```bash
   ./script.sh
   ```
   - Executes the script.



This guide covers essential commands and basic shell scripting techniques essential for anyone learning or using Linux. Practice regularly and explore further to master these tools effectively.

<hr>
<h3 align="center"> 🧑🏻‍💻 | Made By : <a href="https://github.com/mohamedtalhaouii" target="_blank">Mohamed Talhaoui</a></h3>
