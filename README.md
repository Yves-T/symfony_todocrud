todolist
========

A Symfony project based on this tutorial : Building a Symfony 3 App found on youtube

## To set up the database

Create a database named todolist

Edit app/config/parameters.yml.dist and enter the connection parameters for the db

## Steps to create the database entity

The entity is already created for this project but these are the steps

        php bin/console doctrine:generate:entity

A command line app will open to ask some questions

Entity short cut name: AppBundle:Todo
Configuration format: just press enter to accept default ( annotations )

fields

* **name** and accept defaults
* **category** and accept defaults
* **description** and accept defaults
* **priority** and accept defaults
* **due_date** change field type to datetime
* **create_date** change field type to datetime

Press return to stop adding fields

The following entity file is created **src/AppBundle/Entity/Todo.php**

To create the table for the entity run

        php bin/console doctrine:schema:update --force

Reference documentation page for al this:

http://symfony.com/doc/current/book/doctrine.html
