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


Step 2 : Install Postgres 
- Download Postgres for windows from <a href="https://www.enterprisedb.com/downloads/postgres-postgresql-downloads"> Postgres for Windows</a>
- Select Options for Additional Features 

- Select All Optional Features (PGAdmin....)
- Set Password for postgres User  

- Set port if Postgres Default port is selected(Or Use default )

- Install Postgres   



Step 3 : Install Python Dependences 
After Installing Python more documentation [Python 3.6, 3.7, or 3.8](https://www.odoo.com/documentation/14.0/contributing/documentation.html#python)
- Install odoo Python dependencies listed in the file [`requirements.txt`](https://github.com/akradore/odoo-windows/tree/odoo12c/requirements.txt).
In a shell / command promt , navigate to the directory with downloaded `requirements.txt` and run thefollowing command:

   ```sh
   pip3 install -r path/requirements.txt
   ```


Step 4 : 

Step 5 : 






For a standard installation please follow the <a href="https://www.odoo.com/documentation/14.0/administration/install.html">Setup instructions</a>
from the documentation.

To learn the software, we recommend the <a href="https://www.odoo.com/slides">Odoo eLearning</a>, or <a href="https://www.odoo.com/page/scale-up-business-game">Scale-up</a>, the <a href="https://www.odoo.com/page/scale-up-business-game">business game</a>. Developers can start with <a href="https://www.odoo.com/documentation/14.0/developer/howtos.html">the developer tutorials</a>
