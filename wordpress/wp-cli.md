## Installing WordPress using wp CLI.
1. To download WordPress core
```
wp core download
```
2. Creating configuration file (wp-config.php). Don't forget to replace the [YOUR_DB_NAME] with your database name and copy the root directory path then replace it with [YOUR_ROOT_PATH] 
```
wp config create --dbname="YOUR_DB_NAME" --dbuser="root" --dbpass="" --dbhost="localhost" --path="YOUR_ROOT_PATH"
```
[YOUR_ROOT_PATH] should be like *D:\wamp64\www\projects\your-project*
3. These two commands are optional.
```
# You can open wp-config.php on your command line interface
cat wp-config.php
# If you want to shuffle salt keys then run this command
wp config shuffle-salts
```
4. Creating Database
```
wp db create --path="YOUR_ROOT_PATH"
```
5. Installing the WordPress core.  
YOUR_PROJECT_URL = `http://localhost/projects/project_name`  
YOUR_PROJECT_TITLE = WordPress
```
wp core install --url="YOUR_PROJECT_URL" --title="YOUR_PROJECT_TITLE" --admin_user="admin" --admin_password="admin" --admin_email="email@email.com" --path="YOUR_ROOT_PATH"
```
## Commands for CORE
```
# To check wp version
wp core version

# To check core update
wp core check-update

# To update wp core
wp core update

```
## Commands for Database
```
# To check whole database size
wp db size

# To check database tables size
wp db size --tables

# To view all the database tables
wp db tables

# To optimize the database tables
wp db optimize

# To repair database
wp db repair

# To check the database status
wp db check

# To export the whole database. [YOUR_DB_NAME] need to be replaced.
wp db export YOUR_DB_NAME.sql
```
## Commands for Site
```
# To remove all posts and pages
wp site empty

# To change the permalink and flush the rewrite rules
wp rewrite structure '/%postname%/'

# To remove all the comments
wp comment delete $(wp comment list --format=ids) --force

# To set WP_DEBUG status in wp-config.php
wp config set WP_DEBUG true / false

# To set WP_DEBUG_DISPLAY status in wp-config.php
wp config set WP_DEBUG_DISPLAY true / false

# To set WP_DEBUG_LOG status in wp-config.php
wp config set WP_DEBUG_LOG true / false