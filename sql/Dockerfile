FROM mysql
#Create the required database upgradpg
ENV MYSQL_DATABASE upgradpg
#Create the required user with persmissions to access the DB  
COPY ./sql-scripts/ /docker-entrypoint-initdb.d/
