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

`dsup [-u <string>] [-p <string>] [/path/to/database/dump] [database name] [VirtualHost Name] [Link to repo]`
`dsup [-r <VirtualHost Name>]` : Here <Virtual Host Name> should be the name of the virtual host of the drupal instance you wish to delete completely.

### Example

`dsup -u dbusername -p dbpassword /home/user/drupal7.tar.gz drupal7.local git@github.com:someone/drupal7.git`
`dsup -r drupal.local`
## TODO

* Allow to setup a new drupal instance.
