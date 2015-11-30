# About

Script to setup/remove a local instance of a drupal website easily.

This does the following things:

* Import a database in tar.gz format to a new/existing database (will overwrite existing db).
* Clone the git repository of instance to the current directory.
* Create a settings file with given username and password.
* Create virtual host, enable site and restart apache.
* Append the virtual host name to hosts file.
* Deletes an entire drupal instance (database, hosts etc) completely.  
Note: This requires sudo access, but you need not prepend sudo, the script will ask you access either way.  
Note: This script works assuming you have named you VirtualHost conf file as 'virtualhostname.conf' (only for Removing Drupal instance)  
Examples for Virtual host names : drupal-7.local, test-1.com.local, drupal.com (If you're brave enough!), z1.test.drupal.local, dev.something.con, etc etc  
Examples for their conf files : drupal-7.local.conf, test-1.com.local.conf, drupal.com.conf, z1.test.drupal.local.conf, dev.something.con.conf, etc etc  

## Usage

`dsup [-u <string>] [-p <string>] [/path/to/database/dump] [database name] [VirtualHost Name] [Link to repo] [optional/path/fo/drupal/installation]`  
`dsup [-r <VirtualHost Name>]` : Here `<Virtual Host Name>` should be the name of the virtual host of the drupal instance you wish to delete completely.
`dsup [-u <string>] [-p <string>] [-v <version>] [database name] [VirtualHost Name] [optional/path/fo/drupal/installation]`  

### Example

`dsup -u dbusername -p dbpassword /home/user/drupal7.tar.gz drupal7.local git@github.com:someone/drupal7.git`  
`dsup -r drupal.local`  
`dsup -u dbusername -p dbpassword /home/user/drupal7.tar.gz dbname drupal7.local git@github.com:someone/drupal7.git`  

## TODO

* Rollback in case of error

## INSTALL

Open terminal and enter the following commands  
`$ cd /bin`  
`$ sudo ln -s /Path/to/dsup`  
`$ sudo chmod +x /bin/dsup`  

You're good to go! Execute the command dsup from anywhere now.
Run command `dsup` to check the usage.

## NOTES
* This script operates under the asumption that you webroot is in `public_html`
* There is no rollback as of yet. If the script fails while running, you will most likely be attached to another object by an inclined plane, wrapped helically around an axis!
* Please point out mistakes and contribute to help make this better and add more functionalities.
