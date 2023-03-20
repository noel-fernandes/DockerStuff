Docker Stuff
=============

My adventures with dockerizing everything.

Notes
-----
### Environment variable Files
Rename 'env.sample' files to '.env'

### SQL Server
SQL Server container with bound volumes on linux hosts raises permission issues i.e. the containers have no permissions to write into the bound volumes. Throws the following error:

>ERROR Setup FAILED copying system data file 'C:\templatedata\master.mdf' to '/var/opt/mssql/data/master.mdf':  5(Access is denied.)

In order to resolve this, a 'root' user for installation is added.

### Bring up all containers
Traverse to the 'Combined' folder and run <code>docker-compose up -d</code> to bring up all containers.

### Bring up individual containers
Traverse to any one of the individual folders eg: Kafka or MongoDb and run <code>docker-compose up -d</code> to bring up a container.
