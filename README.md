# my-maria-db-dockerized

- mariadb
- phpmyadmin


## MySQL commands

- create new user    
`CREATE USER 'myUser'@'%' IDENTIFIED BY 'myPassword';`

- create new database     
`CREATE DATABASE dbName;`

- grant privilages     
`GRANT ALL PRIVILEGES ON dbName.* TO 'myUser'@'%';`

## Managing DB

- Backup     
`docker exec CONTAINER /usr/bin/mysqldump -u root --password=root DATABASE > backup.sql`
- Restore     
`cat backup.sql | docker exec -i CONTAINER /usr/bin/mysql -u root --password=root DATABASE`
