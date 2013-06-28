About
============================
This script is designed to automate the deployment of WordPress on a fresh (ve) server installation using an Nginx stack.


Overview
============================
This script requires Ubuntu 11.04. It installs and configures the required OS packages and the MySQL/Nginx/PHP-FPM/Postfix deployment stack for WordPress. All packages are installed through aptitude for future upgrade ease.

NOTE: The script disables SSH root login, sets up a sudo user, and optionally changes the SSH port for server security. At the top of the script, you can see the variables that should be set prior to running the script. All variables should have value, otherwise the script will not run.


Usage
============================
1. Download the script files from the GitHub repo as a tar file. 
2. Upload the tar file to /root. 
3. Login to the server as root and untar the file: 
	- tar -xzvf venison.tar.gz
4. Enter setup directory:
	- cd venison
5. Edit script variables for your configuration: 
	- vim setup.sh
	- Edit lines 4-12 to match your needs
	- save the changes
5. sh setup.sh
6. Let it run


Notes
============================
DO NOT LOG OUT of your root session. Once the script has completed, the root user can no longer SSH into the server. You need to use the login for the `sudo_user` you setup in the script variables. So, start a new SSH session and try to login using the account of the `sudo_user`. Once you have confirmed you can login successfully, you can close the root session.


License
============================
Copyright (c) 2011 by TJ Stein 

This program is free software: you can redistribute it and/or modify it under the terms of the MIT License.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.