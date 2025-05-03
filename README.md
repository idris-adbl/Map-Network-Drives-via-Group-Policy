# Map-Network-Drives-via-Group-Policy

1. On Windows 10 machine, after logging in with the credentials of jdoe and password. We need to map the folder.
2. Right click on This PC> Map network drive 
3. Put as Drive: H > Folder: \\WINDOWSSERVER\HR ( put server as you assigned to Windows server machine) > uncheck reconnect at sign-in> finish.
4. Next, we create GPO for our mapped drive.
5. Next, we go to Windows Server machine. On the Group Policy Management> right click on Mapped Driver> Edit> User Configuration> Preferences>windows settings> Drive Maps> Right click on Drive Maps > new> mapped drive> location: \\WINDOWSSERVER\HR > Select drive letter as :H >OK 
6. Now, we will apply this to the specific OU that we want. Just drag and drop the mapped drives folder to the User folder.
7. Lastly, on Windows 10 machine, go to the command line cmd > type gpupdate / force> press enter.

  ![image](https://github.com/user-attachments/assets/ef3d7217-f8a3-4d28-b781-6f048bac8c96)
