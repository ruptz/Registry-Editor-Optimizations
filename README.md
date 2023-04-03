# Registry Editor Optimizations

Open "Registry Editor" on your pc

**BEFORE YOU DO ANYTHING MAKE SURE YOU BACKUP YOUR REGEDIT**

*I am not responsible for anything if you do not save a backup*

Top left "file" then click export and save it to your pc, if you need to put the backup back in your regedit go to "file" top left and click import and import your settings.

## Boosting Performance

*The top of your registry editor you will see a file path, click the file path and paste the following below into it and click enter.*

```HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Multimedia\SystemProfile```

*Next you will see 3 files but you will only change 2*

```
NetworkThrottlingIndex

SystemResponsiveness
```

*You will want to change the values of both the files to the ones below*

```
NetworkThrottlingIndex
Hexadecimal value: ffffffff

SystemResponsiveness
Hexadecimal value: 0
```

## Next step

*You will see files on the left, there will be a tasks folder. Go into tasks folder and you will see a folder inside the tasks folder named "Games" and then open the games folder.*

You will see 8 files, but will only want to change the 4 listed below

```
GPU Priority
Priority
Scheduling Category
SFIO Priority
```

*Listed below will be the values you will want to change them to*

```
GPU Priority = 8
Priority = 6
Scheduling Category = High
SFIO Priority = High
```

# Reduce network latency

At the top of your registry editor again click the file path and paste the one below and click enter

``` HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\services\Tcpip\Parameters\Interfaces ```

Next, find your ipv4 address. you will see files on the left will have random numbers and weird file names, find the folder with ```DhcpIPAddress``` with the correct ipv4 IP Address you saw when you looked yours up.

Next you will want to create 2 new files in that folder.

Right click in a open space and press ```NEW```, You will now see a bunch of stuff you can select but want to create 2 ```DWORD (32-bit) Value``` files.

After you create them rename them by selecting the file and pressing ```F2``` to rename the file. 

*Rename the files to the 2 names listed below*

```
TcpAckFrequency

TCPNoDelay
```

*You will now want to set both of the values for the files by double clicking on them and changing them both to a 1 value*

```
TcpAckFrequency = 1

TCPNoDelay = 1
```
*If you are confused at all by anything please let me know and I can describe it better for you in the read.me*

Discord: ruptz#7777
