# Owncloud auto deploy via ansible Document with SSL #

## Pure environment #
  
```
This playbook will auto install Mysql,Nginx,php5-fpm,owncloud.
```
    
### Before run this playbook: #
    
#### Check the **vars:** section in playbook.yml #
-------------------------------------------------
##### 1.**mysql_root_password: "11111111"**. #
  The "11111111" is a default password for *root* of MySQL.
  __Don't forget to change password after Ansible run over.__
  
-------------------------------------------------
##### 2.**owncloud_account: "owncloud"**. 
  It means Ansible will create a database user for owncloud.
  
  The username is *owncloud*.
  
-----------------------------------------------
##### 3.**owncloud_password: "12345678"**.
   The owncloud's password in database. You can change it.
   
-----------------------------------------------
##### 4.**owncloud_server_name: "owncloud.biotrump.com"**.
   Server name for you ownclound. It setting in nginx "etc/nginx/sites-available/redir-owncloud".
   
   You can change it.
   
----------------------------------------------
### After run playbook.yml #

 * Use web browser and type *owncloud.biotrump.com* to link to owncloud service.
 
    That will show **an unsafe or private authority connection** . Just **conntinue connect and go on**
    
    then own the owncloud.

## If you have MySQL ! :

### Before run this playbook: #

#### Check the **vars:** section in playbook.yml #
-------------------------------------------------
##### 1.**mysql_root_password: "11111111"**. #
  Change the password to your *root's* of MySQL.
  The Ansible will create a database for owncloud.
  
  __Don't forget to change password back after Ansible run over in playbook.yml__
  
-------------------------------------------------
##### 2.**owncloud_account: "owncloud"**. 
  It means Ansible will create a database user for owncloud.
  
  The username is *owncloud*.
  
-----------------------------------------------
##### 3.**owncloud_password: "12345678"**.
   The owncloud's password in database. You can change it.
   
-----------------------------------------------
##### 4.**owncloud_server_name: "owncloud.biotrump.com"**.
   Server name for you ownclound. It setting in nginx "etc/nginx/sites-available/redir-owncloud".
   You can change it.
   
----------------------------------------------
### After run playbook.yml #

 * Use web browser and type *owncloud.biotrump.com* to link to owncloud service.
 
    That will show **an unsafe or private authority connection** . Just **conntinue connect and go on**
    
    then own the owncloud.