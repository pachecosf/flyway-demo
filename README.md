## Demo to show how easy it is to manage mysql with docker and flyway

Flyway is "version control for you database". It allows you to add sql scripts to a 
repository. Once there flway will query the database compare what scripts have been 
executed, and executes anything not executed on the database. It uses checksums on 
the previously applied migrations, so once a sql script has been executed, you can't go back and edit an already applied migration.

This repo is a simple demo of how to use flyway docker images, with a migration
folder to version a mysql database. I've also included a script to cleanup any
docker volumes created by previous startups, if you want to start fresh.

To run:
`docker-compse up`