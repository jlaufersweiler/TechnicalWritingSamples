*****************************OVERVIEW**********************************
The ALF Helpers are a handful of simple tools to perform pre-proccessing
tasks that are helpful to many of our clients, and launch a group of 
related ALF broadcasts.

Enclosed in this archive are the follofing items:

lunch.bat	-script for processing data files and launching ALF for lunch calls.
		-moves files to working directory, then calls filesplit.exe and ALF.exe

lunch_cfg.bat	-configuration file for lunch.bat

attend.bat	-script for processing data files and launching ALF for attendance calls.
		-moves files to working directory, then calls namejoin.exe and ALF.exe

attend_cfg.bat	-configuration file for attend.bat

File Splitter	-Folder containing filesplit.exe, software that splits records from
		-lunch data files into seperate files based on instance count of unique numbers.

Name Joiner	-Folder containing namejoin.exe, software that merges first names 
		-in attendance data files for records where phone numbesr are identical

Files		-Empty forlder for use as working directory.
 


*******************************SETUP**********************************

setup is fairly simple:

1)	Extract the contents of this archive, and place them in the same folder
	that contains your "ALF All Files" folder (though not IN "ALF All FIles")

2) 	Edit the lunch_cfg.bat and attend_cfg.bat files to match your environment
	as needed, but leave the ALF_CIDS variable as NONE for now.
	(Right-Click on the .BAT files and choose EDIT to open in Notepad)

3)	Run lunch.bat and attend.bat for testing.  Files will be processed, but no
	calls will be launched.

4)	Run the ALF Config Tool to point a broadcast at each of the generated 
    	files for each school in Files. Take note of the config ID for each
	broadcast.

5)	Edit the lunch_cfg.bat and attend_cfg.bat files with the appropriate config
	IDs from the ALF config Tool, and uncomment the last few lines.
	
5)	Set up a Scheduled Task each to run lunch.bat and attend.bat at the times
	of your choosing.


For more information, refer to the README.TXT files in the File Splitter and 
Name Joiner folders, or Right-Click on the .BAT files and choose EDIT to view 
detailed comments within.


