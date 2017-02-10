# PiControl

PiControl is a web control centre written in PHP for Raspberry Pi.

This is the modified version of the orignal Raspcontrol by Bioshox - It appears the repo is no longer available and the original version isn't working any more.

***

## Installation
If you have no webserver yet, run `sudo apt-get update && sudo apt-get install apache2 php5` to install Apache and PHP.

After you installed the server, you can just copy the project to `/var/www/html`.

Now you have to setup the access to the control panel. 
Execute `sudo mkdir /etc/picontrol && sudo nano /etc/picontrol/database.aptmnt` to create the user database and add the following lines:

	{
 	   "user":       "yourName",
 	   "password":   "yourPassword"
	}
Obviously, replace 'yourName' and 'yourPassword' with your own values. This will be your future login credentials for the interface.

Press `Ctrl-X`, `Y` and `Enter` to save and exit the editor.

Finally, correct the permissions of the newly created file by executing `sudo chmod 740 /etc/picontrol/database.aptmnt && sudo chown www-data:www-data /etc/picontrol/database.aptmnt`.
***

## Optional configuration

In order to have some beautiful URLs, you can enable URL Rewriting.
__Note:__ It's NOT necessary to enable URL Rewriting to use PiControl.
l.
