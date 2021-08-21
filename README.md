# Run Odoo without Installing : Windows
 
[![Build Status](http://runbot.odoo.com/runbot/badge/flat/1/master.svg)](http://runbot.odoo.com/runbot)
[![Tech Doc](http://img.shields.io/badge/master-docs-875A7B.svg?style=flat&colorA=8F8F8F)](http://www.odoo.com/documentation/master)
[![Help](http://img.shields.io/badge/master-help-875A7B.svg?style=flat&colorA=8F8F8F)](https://www.odoo.com/forum/help-1)
[![Nightly Builds](http://img.shields.io/badge/master-nightly-875A7B.svg?style=flat&colorA=8F8F8F)](http://nightly.odoo.com/)

Running Odoo on Windows Machine without Installation
------------------------------------------------------

This Method will work best for developers using Microsoft Windows. Odoo is a suite of web based open source business apps.

Odoo Apps can be used as stand-alone applications, but they also integrate seamlessly so you get
a full-featured <a href="https://www.odoo.com">Open Source ERP</a> when you install several Apps.


Getting started with Odoo on Windows without installation
----------------------------------------------------------

### Requirements

- [Git](https://www.odoo.com/documentation/14.0/contributing/documentation.html#install-git)
- [Python 3.6, 3.7, or 3.8](https://www.odoo.com/documentation/14.0/contributing/documentation.html#python)
- Python dependencies listed in the file [`requirements.txt`](https://github.com/akradore/odoo-windows/tree/odoo12c/requirements.txt).
- [Make](https://www.odoo.com/documentation/14.0/contributing/documentation.html#make)
- A local copy of the [odoo/odoo repository in 14.0](https://github.com/odoo/odoo/tree/14.0) (Optional)


This guide covers the steps necessary for configuring and running Multiple Odoo Versions for development using Git source
To run Odoo on windows you just follow the below steps for all versions of Odoo .

<b>Step 1 : Install Python</b>

- Download Python for windows from <a href="https://www.python.org/downloads/windows/"> Python for Windows</a>
- Click Option Add Python to Path

- Select Customize Installation

- Select All Optional Features 

- Advanced Option : Install foa all Users
 
- Change Installation Location to <b>C:\Python\Python37</b>


<b>Step 2 : Install Postgres & Create User openpg in postgres </b>
- Download Postgres for windows from <a href="https://www.enterprisedb.com/downloads/postgres-postgresql-downloads"> Postgres for Windows</a>
- Select Options for Additional Features 

- Select All Optional Features (PGAdmin....)
- Set Password for postgres User  

- Set port if Postgres Default port is selected(Or Use default )

- Install Postgres   

- Run PGAdmin and create User role `openpg` with password `openpgpwd` in Postgres



<b>Step 3 : Install Python Dependences </b>
After Installing Python more documentation [Python 3.6, 3.7, or 3.8](https://www.odoo.com/documentation/14.0/contributing/documentation.html#python)
- Install odoo Python dependencies listed in the file [`requirements.txt`](https://github.com/akradore/odoo-windows/tree/odoo12c/requirements.txt).
In a shell / command promt , navigate to the directory with downloaded `requirements.txt` and run thefollowing commands:

   ```sh
   pip install -r (`path`)/requirements.txt
   ```
   ```sh
   pip install libsass
   ```
   ```sh
   pip install gevent
   ```
   ```sh
   pip install greenlet
   ```
   ```sh
   pip install numpy
   ```
   ```sh
   pip install ptvsd
   ```
   ```sh
   pip install reportlab
   ```



<b>Step 4 : Running Odoo : Using Terminal/Powershell </b>

In order to understand `odoo-bin` options read the following options <a href="https://www.odoo.com/documentation/14.0/develSince there is no config file the following options are critical in Options</a> 

- In My video Im using Visual Studio to run odoo without installation, this can be in 2 possible ways:

1. Run Odoo Using Odoo-bin Options 
    - To Running Odoo use the following commands :  
    ```sh
   python  C:\Users\Laptop\Desktop\odoo12c\server/odoo-bin   --db-filter 12adore.* --db_port=5432 --db_user=openpg --db_password=openpgpwd  --xmlrpc-port=9012 --addons-path=C:\Users\Laptop\Desktop\odoo12c\server\odoo\addons --logfile  C:\Users\Laptop\Desktop\odoo12c\odoo.log

   ``` 
    Since there is no config file the following options are critical: `--db_port=`postgres port ,  `--db_user=`postgres user, `--db_password=`postgres password  ,`--xmlrpc-port= `odoo browser port ,` --addons-path=`addons path ,` --logfile` .

2. Run Odoo Using Config file  
    - To Running Odoo use the following commands :  
    ```sh
   python C:\Users\Laptop\Desktop\odoo12c\server/odoo-bin  -c C:\Users\Laptop\Desktop\odoo12c\server\odoo.conf

   ``` 
    Since the config file is defined all odoo-bin options are also defined in the the config file however in your command you need to define the config file path with a `-c` odoo-bin option. 
- In My video Im using Visual Studio
Step 5 : 






For a standard installation please follow the <a href="https://www.odoo.com/documentation/14.0/administration/install.html">Setup instructions</a>
from the documentation.

To learn the software, we recommend the <a href="https://www.odoo.com/slides">Odoo eLearning</a>, or <a href="https://www.odoo.com/page/scale-up-business-game">Scale-up</a>, the <a href="https://www.odoo.com/page/scale-up-business-game">business game</a>. Developers can start with <a href="https://www.odoo.com/documentation/14.0/developer/howtos.html">the developer tutorials</a>
