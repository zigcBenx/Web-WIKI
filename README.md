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
      
  __How can I get phpmyadmin__
  
  PHP myadmin is administration tool for easy access to your database collection.
  You can install it by installing LAMPP(Linux,Apache,Mysql,Perl and PHP) or WAMPP for Windows.
  > This instructions are focused on Linux users only!
  
  1. Try running:
      ```
      sudo /opt/lampp/lampp start
      ```
      
      If this shows you log of mysql, apache and some other stuff with status __OK__ than you are done! Go to last step.
  
  2. If that is not the case for you, don't worry, it's probbably another server already running, check for running services:
      ```
      service --status-all
      ```
      
      If you see '+' sign infront of apache2 or something similar this is the problem! All you need to do is stop it by running:
      
      ```
      sudo service stop apache2
      ```
      
      Than go to step 1 and you are good to go!
  
  3. Go to your browser at: http://localhost/phpmyadmin
     This should show you your administration panel.

### SSH
  __SSH to server__
  1. Open your terminal / command line and run:
      ```
      ssh user@servername -p portnumber
      ```
  2. Type password for your server

### PHP

#### Laravel
  __clone project from github__
  1. `cd` to folder you want to save this project
  2. get clone link at right top corner o github page and run:
      ```
      git clone clonelink
      ```
  3. `cd` to folder that was cloned
  4. Run command:
      ```
      composer install
      ```
      for installing all dependecies.
  5. Go to your favourite sql administration panel (phpmyadmin) and create new database. - look at section how can I get phpmyadmin?
  6. Copy .env.example to .env
      ```
      cp .env.example .env
      ```
  7. Run:
      ```
      php artisan key:generate
      ```
  8. Set your database credetials that you setup in previous steps in .env file
  9. Run:
      ```
      php artisan migrate
      ```
      for migrating database.
      If you already have some tables in database and want to "remigrate" run:
      ```
      php artisan migrate:fresh
      ```
      If project that you have cloned provide seeded data run:
      ```
      php artisan migrate --seed
      ```
  10. And finally run:
      ```
      php artisan serve
      ```
      to run your localhost server
  
      
TODO: Download from quickadminpanel and setup vue ect.

## CSS hints
change color of image to back and white:
`-webkit-filter: opacity(60%) grayscale(100%) contrast(10%);
filter: opacity(60%) grayscale(100%) contrast(10%);`

## JS hints
Check if all element in array are the same. Or all objects have the same property:
```
return materials.every(
        (v) => v.price === materials[0].price
      )
```

## VUE hints
search object by key value
 // configs is array of objects
 // this.config_id is value by which we are searching object
`_.find(this.configs, {id: this.config_id});`
