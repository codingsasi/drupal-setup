# About

Script to setup a local instance of a drupal 7 website easily.

This does the following things:

* Import a database in tar.gz format to a new/existing database (will overwrite existing db).
* Clone the git repository of instance to the current directory.
* Create a settings file with given username and password.
* Create virtual host, enable site and restart apache.
* Append the virtual host name to hosts file.
* Deletes an entire drupal instance (database, hosts etc) completely.
Note: This requires sudo access, but you need not prepend sudo, the script will ask you access either way.

## Usage

`dsup [-u <string>] [-p <string>] [/path/to/database/dump] [database name] [VirtualHost Name] [Link to repo] [optional/path/fo/drupal/installation]`  
`dsup [-r <VirtualHost Name>]` : Here <Virtual Host Name> should be the name of the virtual host of the drupal instance you wish to delete completely.
`dsup [-u <string>] [-p <string>] [-v <version>] [database name] [VirtualHost Name] [optional/path/fo/drupal/installation]`  

### Example

`dsup -u dbusername -p dbpassword /home/user/drupal7.tar.gz drupal7.local git@github.com:someone/drupal7.git`  
`dsup -r drupal.local`  
`dsup -u dbusername -p dbpassword /home/user/drupal7.tar.gz dbname drupal7.local git@github.com:someone/drupal7.git`  

## TODO


## INSTALL

Open terminal and enter the following commands
`$ cd /bin`  
`$ sudo ln -s /Path/to/dsup`  
`$ sudo chmod +x /bin/dsup`  

You're good to go! Execute the command dsup from anywhere now.
Run command dsup to check the usage.
