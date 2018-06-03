# OSSEC-GUI
Version of OSSEC-WUI adapted to OSSEC versions >= 2.9.3, V3.0 included.
This an evolution from Analogi (from Ecsc) and OSSEC-WUI which can be found at :
https://github.com/NunesGodinho/OSSEC-WUI which uses the "old" database schema.
The software is in final tests with both versions 2.9.3 and V3.0 stable.
Should be released soon.
This version contains new functions :
- Some statistics.
- Ability to remove alerts.
- Ability to "reorganize" the database in a dedicated function.
- Functions to manage signatures/category mapping.
- Management of authentication with three levels to manage rights to access many functions.
- A new improvement : ability to use two databases, one "running" which is feeded by OSSEC where you can "delete" records that are no more interesting (problems solved ...). 
All deleted records are automagically re-inserted in the second ("history") database for statistical and historical access, thanks to a simple "trigger" on the "alert" table.
- Some improvements in managing Sql

The project uses :
- Amcharts for tracing graphs (as Analogi and OSSEC-WUI) : https://www.amcharts.com
- PHP AUTH from Delight-im for managing authentication : https://github.com/delight-im/PHP-Auth

To use it you must install : 
- A Web server with PHP enabled (Tested with Apache 2.4.25 on a Debian Stretch)
- A Mysql database (tested with Mysql 5.7 and Mariadb 10.3).
