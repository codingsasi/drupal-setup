# About

Script to setup a local instance of a drupal 7 website easily.

This does the following things:

* Import a database in tar.gz format to a new/existing database (will overwrite existing db).
* Clone the git repository of instance to the current directory.
* Create a settings file with given username and password.
* Create virtual host, enable site and restart apache.
* Append the virtual host name to hosts file.

Note: This requires sudo access

## Usage

`dsup [-u <string>] [-p <string>] [/path/to/database/dump] [database name] [Virtual Host Name] [Link to repo]`

### Example

`dsup -u dbusername -p dbpassword /home/abhai/drupal7.tar.gz drupal7.local git@github.com:someone/drupal7.git`

## TODO

* Allow to setup a new drupal instance.
