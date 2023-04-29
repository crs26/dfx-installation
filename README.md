# Getting started on Internet Computer

## Installing Canister SDK

### Windows Installation
1. Search for terminal and run it as administrator.  
	![image](https://user-images.githubusercontent.com/55611653/235280652-67872dcd-d500-4b02-9997-9c7e667b9daf.png)
2. Enable feature `Windows Subsystem for Linux` (WSL).
	```
	dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
	```
3. Set WSL version 2 as default.
	```
	wsl --set-default-version 2
	```
4. Install ubuntu linux
	```
	wsl --install
	```
5. Run ubuntu terminal  
	![image](https://user-images.githubusercontent.com/55611653/235281427-f90d296a-3ed6-4229-8757-4fea81e5853e.png)
		
	If you encountered an error `WslRegisterDistribution failed with error: Ox80370114`  
	</br>
		![Screenshot 2023-04-28 164514](https://user-images.githubusercontent.com/55611653/235281554-981dca48-1109-45c6-bd11-cc9f1f8c42b2.png)  
	Enable the `Hyper-V` feature. If no error occured do not execute this command.
	```
	dism.exe /online /enable-feature /featurename:Microsoft-Hyper-V /norestart
	```  
	If no errors occured you should see the welcome message of ubuntu linux  
	</br>
	![Screenshot 2023-04-28 165623](https://user-images.githubusercontent.com/55611653/235283424-0f6e0687-48b4-4432-9a9a-d7ffd13336f8.png)

6. Add `NodeJS` to package repository
	```
	sudo sh -ci "$(curl -fsSL https://deb.nodesource.com/setup_18.x)"
	```
7. Install `NodeJS`
	```
	sudo apt install nodejs
	```
8. Install `dfx`
	```
	sh -ci "$(curl -fsSL https://internetcomputer.org/install.sh)" 
	```
9. Update path to easily execute `dfx` command
	```
	PATH="$PATH:$HOME/bin"
	```
10. Verify that `dfx` is properly installed
	```
	dfx --version
	```
	![image](https://user-images.githubusercontent.com/55611653/235283664-af418229-a511-465d-9889-a658db2a2796.png)
