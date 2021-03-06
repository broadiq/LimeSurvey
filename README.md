# How to use this image

This image is meant to be used with BroadIQ. Please go to BroadIQ and create an account if you don't have one. Then you can use BroadIQ's tools to deploy the image.

# LimeSurvey

This is a basic image of Limesurvey build on top of php:7-apache official image. I've added prerequisite libraries (gd,zip,ldap,imap) and PDO for mysql.

No database included, this image aim to be used with an external database.

You can export upload dirs to docker volumes, it'll be useful to update your installation with a newest image.


# Environment variables

Environment variables are basicaly the ones that can be found in config.php after the LimeSurvey wizard.

* `WIZARD_BYPASS` : `true` if you want to specify your existing Database. `false` for LimeSurvey wizard, if it's your first install.
* `LS_DEBUG` : Set this to `1` if you are looking for errors. Set this to `2` if you want to enable SQL debugger too.
* `LS_DEBUGSQL` : Set this to 1 to enanble sql logging, only active when `LS_DEBUG` = 2.
* `LS_DB_DRIVER` : Database driver to use (e.g. `mysql`, `pgsql`, `mssql`, `sqlite`, `oci`)
* `LS_DB_HOST` : Database hostname. Probably the name of an another database container linked to this one.
* `LS_DB_PORT` : Database port (e.g. 3306 for MySQL)
* `LS_DB_NAME` : Database name
* `LS_DB_USER` : The username used to connect to the database
* `LS_DB_PASSWD` : The password used to connect to the database
* `LS_DB_CHARSET` : Charset of you database, depends of your database configuration.
* `LS_DB_PREFIX` : You can add an optional prefix, depends on how your tables have been created.
* `BASE_URI` : Alias URI after the domain. (e.g. "/limesurvey" )
* `PUBLIC_FQDN` : Public domain in case of reverse proxy

