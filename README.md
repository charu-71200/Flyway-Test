# Flyway-Test

Flyway is an open-source database migration tool.

Flyway allows us to change our database by running a set of scripts in a defined order. These scripts are called 'migrations' as they allow us to 'migrate' our database from one version to another. 
In this project I have implemented FLyway with a gradle type project.
Initial set up is easy as we just need to add a plugin and some configuration related to flyway in build.gradle.
And then we can write migration scripts, like here I have written 3 Migration scripts in src/main/resources/db/migration namely : 
V1__create_table
V2__add_data
V3__create_table
Every time the need to upgrade the database arises, whether it is the schema (DDL) or reference data (DML), we can simply create a new migration script with a version number higher than the current one. When Flyway starts, it will find the new script and upgrade the database accordingly.
