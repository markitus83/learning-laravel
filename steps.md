# Steps (Codeanywhere environment)
----
* Install Laravel
`composer create-project --prefer-dist laravel/laravel my-project-name "5.5.*"`

* Edit DocumentRoot and working directory on Apache
`sudo vim /etc/httpd/conf/httpd.conf`
-DocumentRoot must change to public folder in your project 
 `"home/cabox/workspace/my-project-name/public"`
-Working directory must change to your project
`"home/cabox/workspace/my-project-name"`
-Restart Apache
`sudo apachectl restart`

* Change permission of storage and cache directories
`chmod -R ugo+rw my-project-name/storage/`
`chmod -R ugo+rw my-project-name/bootstrap/cache/`

* App key
`cp my-project-name/.env.example my-project-name/.env`
-Inside your project folder
`php artisan key:generate`