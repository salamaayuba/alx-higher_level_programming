Introduction to MySQL in Python
MySQL Python is the MySQL driver for the Python language. It is broken down into two parts, a wrapper library _mysql and the DB-API 2.0 module MySQLdb. All we are concerned with as developers integrating MySQL into our Python scripts is the DB-API module MySQLdb.

The module MySQLdb conforms to the standards set by the Python PEP 249. This is a standard to help promote database development in Python and make integrating with multiple databases much easier. The idea is similar to JDBC in Java.

The first step to using MySQLdb is to install it on your system. If you are using Linux, check your distribution to see if it has its own precompiled binaries you can use to install the module. If you are using Windows there is a installer that you can download from the Sourceforge project for MySQL Python. If you are using Mac OSX you should check out PythonMac.org. They may have binaries for your particular version.

I don't recommend using this methond of installation unless you know what you are doing. I especially do not recommend trying to install from source on Windows, unless you are using Cygwin.

To install from source, first get the source from the Sourceforge site. Next make sure you have gcc, make, and the standard suite of compilation tools installed on your computer. Now make sure you have all of the prerequsites installed. You need Python 2.3.4 or greater and its development files (python-devel), the MySQL 4.0 or greater libraries with the development files (mysql-devel), and zlib with it's development files (zlib-devel). If you get any compilation errors you are most likely missing one of these prerequisites. If you installed the prerequisites from source, make sure the compile tools are looking in the correct locations. If you installed from binaries make sure you have the associated -devel files installed. They need to be installed seperately. For more specific installation instructions see the README included with the source package.

?
1
2
3
4
tar zxf MySQL-python-x.x.x.tar.gz
cd MySQL-python-x.x.x
python setup.py build
sudo python setup.py install # or su first
To test the installation, open a command prompt or shell. Enter the Python interactive interpreter and import the MySQLdb module. If this returns without error, then you are all set. If not go back and try to reinstall the MySQLdb package.

?
1
2
3
4
5
python
Python 2.4.1 (#1, Sep 13 2005, 00:39:20)
[GCC 4.0.2 20050901 (prerelease) (SUSE Linux)] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> import MySQLdb
The last basic thing that you need to know is that to be able to use the MySQLdb module in any of your packages you just place the 'import MySQLdb' line at the top of your script. That's all.

In the next section I am going to cover making a connection to a MySQL database.
