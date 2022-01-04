# ansible_lamp-stack_wordpress-site

```yml
# ansible-playbook -i ./../inventory main.yml 

PLAY [Install LAMP Stack for WP site] ******************************************************************************************

TASK [Gathering Facts] *********************************************************************************************************
ok: [172.31.39.44]

TASK [include_tasks] ***********************************************************************************************************
included: /home/ec2-user/day-5/apache_setup.yml for 172.31.39.44

TASK [Installing apache and php Packages] **************************************************************************************
changed: [172.31.39.44]

TASK [Install latest php from AMAZON repo] *************************************************************************************
changed: [172.31.39.44]

TASK [setup vhost for wp site] *************************************************************************************************
changed: [172.31.39.44]

TASK [Creating Doc Root] *******************************************************************************************************
changed: [172.31.39.44]

TASK [Download wp data] ********************************************************************************************************
changed: [172.31.39.44]

TASK [Copy wp files to Doc Root] ***********************************************************************************************
changed: [172.31.39.44]

TASK [Wordpress - Creating wp-config.php] **************************************************************************************
changed: [172.31.39.44]

TASK [Start and enable services] ***********************************************************************************************
changed: [172.31.39.44]

TASK [include_tasks] ***********************************************************************************************************
included: /home/ec2-user/day-5/mariadb_setup.yml for 172.31.39.44

TASK [Installing Mariadb and python mysql module] ******************************************************************************
changed: [172.31.39.44]

TASK [Starting and Enabling MariaDB server] ************************************************************************************
changed: [172.31.39.44]

TASK [setup mysql root password] ***********************************************************************************************
[WARNING]: Module did not set no_log for update_password
changed: [172.31.39.44]

TASK [creating my.cnf file] ****************************************************************************************************
changed: [172.31.39.44]

TASK [remove anonymous user] ***************************************************************************************************
changed: [172.31.39.44]

TASK [Removing Test User] ******************************************************************************************************
changed: [172.31.39.44]

TASK [creating wp db  wordpress] ***********************************************************************************************
changed: [172.31.39.44]

TASK [creating DB user wordpress] **********************************************************************************************
changed: [172.31.39.44]

TASK [Post-Installation - CleanUp] *********************************************************************************************
ok: [172.31.39.44] => (item=/tmp/wordpress.tar.gz)
changed: [172.31.39.44] => (item=/tmp/wordpress)

TASK [Post-Installation - Restarting] ******************************************************************************************
changed: [172.31.39.44] => (item=httpd)
changed: [172.31.39.44] => (item=mariadb)

PLAY RECAP *********************************************************************************************************************
172.31.39.44               : ok=21   changed=18   unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
```
![image](https://github.com/Jisjo/ansible_lamp-stack_wordpress-site/blob/main/Screenshot-1.png)
