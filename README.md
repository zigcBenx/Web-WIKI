# Web-WIKI
This is my personal wiki page for webdevelopment you can freely add anything you want.

## Table of content

todo

### MYSQL
  __Connecting to mysql via terminal / command line__
  1. Connect to your server via terminal (SSH to server)
  2. Run: 
      ```
      mysql -u username -p'password'
      ```
      > Password has to be part of tag -p and it does not have to use single quotes.
  __Begin with development__
  1. If you don't know which databases already exist run:
      ```
      show databases;
      ```
  2. To use one of listed databases run:
      ```
      use databasename;
      ```
  3. To list tables run:
      ```
      show tables;
      ```
  > From here on is only basic SQL for CRUD operations.
  Exit mysql with:
      ```
      exit;
      ```
### SSH
  __SSH to server__
  1. Open your terminal / command line and run:
      ```
      ssh user@servername -p portnumber
      ```
  2. Type password for your server
