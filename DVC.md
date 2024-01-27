->	pip install dvc

-> 	git init (for initializing git)
-> 	dvc init (for initializing dvc)


-> you must have folder for keeping all data inside the project 
   let's consider that you have folder named "data"


	Mode                 LastWriteTime         Length Name
	----                 -------------         ------ ----
	d-----        27-01-2024     16:50                data
	d-----        27-01-2024     16:51                DVersion


-> Assuming you have data already present in data folder 
   you have to run the command
   
   	dvc add <path/to/data.file>
   
   this command has added you data.file to dvc environment

   the above command will also prompt you to run following command
   
	git add <path/to/data.file>.dvc <path\to\data\folder>\.gitignore

   these two command will stage the progress into git 


-> Now to push data into our own seperate remote storage or database repository
   
   We need to setup an remote origin for dvc same as the one we use for git

   Syntax of adding remote to DVC
	dvc remote add --default <local name (e.g Origin)> gdrive://<Key of Folder in Gdrive where you want to store>


-> After you successfully add setup remote run below command as it is 
	git commit .dvc\config -m "Configured Remote"
   
-> To push the data to remote
	dvc push

if you are pushing for first time it will prompt you to authentication by google in your default browser
   or 
if you get error
    unexpected error - gdrive is supported, but requires 'dvc-gdrive' to be installed: No module named 'dvc_gdrive'

then you must install that dependency with command
    pip install dvc_gdrive


-> wait for some time then then again run 
	dvc push (authenticate yourself)
   wallah! you just pushed your data to remote repository




-> For cloning the data files right from remote repository
	
	suppose you want to clone it into new project "Data Versioning Clone"
	
	run 
		git init

	run 
		dvc init

	run 
			dvc get https://github.com/Hardik7843/DataVersioning  <github path> -o <local path>
	

