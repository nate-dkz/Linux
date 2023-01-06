# Introduction
This file contains a collection of Linux commands that I have found to be useful. 
I have gathered these commands in one place as a reference point to refer back to whenever I need them.

<details>
<summary><b><font size="+1">System</Shell></b></summary>
</br>

Find out which shell is being used.

``echo $SHELL``

</details>
<details>
<summary><b><font size="+1">System</font></b></summary>
</br>

Displays the uptime of the system.

``uptime``

Displays system information.

``uname -a``

Displays CPU information.

``cat /proc/cpuinfo``

Displays memory information.

``free -h``

Displays disk information.

``df -h``

Displays the status of a service using the system manager.

`` systemctl status <service>``

Restarts a service using the system manager.

`` systemctl restart <service>``

Shuts down the system now.

``shutdown now``

Restarts the system now.

``shutdown -r now``

Restarts the system in 10 mins.

``shutdown -r 10``

Displays log file entries.

``journalctl``

Follows log file entries.

``journalctl -f``

</details>

<details>
<summary><b><font size="+1">Processes</font></b></summary>
</br>

Displays a list of processes for all users.

``ps aux``

</details>

<details>
<summary><b><font size="+1">Network</font></b></summary>
</br>

</details>

<details>
<summary><b><font size="+1">Users</font></b></summary>
</br>

Runs as the root user.

 ``sudo su``

Displays a list of recent user sessions.

 ``last``

Displays information about the current user session.

 ``who``
</details>

<details>
<summary><b><font size="+1">Files</font></b></summary>
</br>

Displays directory size for a file or directory.

``du -h <file>``

Displays file and directory size for all files.

``du -h``

Displays total file and directory size.

``du -sh``

Displays information about a file.

``stat <file>``

Displays the file type for a file.

``file <file>``

Displays files created within the past 90 days, doesn't show hidden files and sorts the files using the ls command.

``find <filepath> -type f -newermt '90 days ago' ! -name '.*' -print0 | xargs -0 ls -lht``

Displays files created within the past 90 days, doesn't show hidden files and copies the files to the specified location using the exec option.

``find <filepath> -type f  -newermt '90 days ago' ! -name '.*' -exec cp {} <filepath> ;``

</details>


