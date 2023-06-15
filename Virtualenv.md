Hello everyone in this article you will be introduced to commands used for working with virtualenv. this tutorial covers everything right from the installation to activation\deactivation of virtualenv
1. How to install virtualenv ? ***Recomended to do this from powershell***
	```
	PS C:\Users\hardi\Downloads> pip install virtualenv
	```

2. How to create new virtual environment ? with name 
**_myenv_** in windows Windows.
	```
	PS C:\Users\hardi\Downloads> virtualenv myenv
	```
	After successfull execution you will get one folder named **_myenv_** in current directory.

3. How to activate virtualenv from windows powershell ?
	``` 
	PS C:\Users\hardi\Downloads> myenv\Scripts\activate.ps1
	```
	after successfull exectution you will observe this in power shell
	```
	(myenv) PS C:\Users\hardi\Downloads>
	```	


4. How to activate virtualenv from cmd or any terminal ?
	```
	C:\Users\hardi\Downloads> myenv\Scripts\activate.bat
	```
	after successfull exectution you will observe this in powershell
	```
	(myenv) C:\Users\hardi\Downloads>
	```

5. How to deactivate virtualenv ? this is same for Powershell , cmd and MacOS/Linux too.
	```
	(myenv) PS C:\Users\hardi\Downloads> deactivate
	```
	after successfull exectution you will observe this 
	```
	PS C:\Users\hardi\Downloads>
	```


6. How to activate virtualenv in MacOS/Linux?
	```
	source myvenv/bin/activate
	```

