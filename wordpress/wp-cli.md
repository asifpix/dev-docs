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