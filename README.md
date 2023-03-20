Docker Stuff
=============

My adventures with dockerizing everything.

Notes
-----
### SQL Server
SQL Server container with bound volumes on linux hosts raises permission issues i.e. the containers have no permissions to write into the bound volumes. Throws the following error:

>ERROR Setup FAILED copying system data file 'C:\templatedata\master.mdf' to '/var/opt/mssql/data/master.mdf':  5(Access is denied.)

In order to resolve this, a 'root' user for installation is added.