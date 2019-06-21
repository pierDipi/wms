# WMS 
### Windowed Management System
## Laravel-KendoUI (Web Desktop-Like Application Environment)

[![GitHub All Releases](https://img.shields.io/github/downloads/simonecosci/wms/total.svg)](https://packagist.org/packages/simonecosci/wms)

<p align="center"><img src="http://www.simonecosci.com/storage/app/media/logo_wms.svg"></p>
<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"><img src="https://telerikhelper.files.wordpress.com/2015/03/kendoui.png?w=440"></p>
<p align="center"><img src="http://www.simonecosci.com/storage/app/media/SS-1.JPG"></p>

## About WMS (Whatever Management System)

*WMS* has been built on top of the *Laravel Framework* by extending some feature and using kendo-ui as frontend javascript framework.
Basically WMS creates for you an *environment* very similar to your *deskto*p for the *administrative backoffice*.
The public area it's up to you.

Using this tool you don't need to be a skilled programmer. 
You just need to have knowledgebase of *relational databases* and that's all.
The application code, for every new module you are going to create, is generated by the application itself.
The owner is called to simply create visually the *data models* and click buttons to scaffold the source code.


*NO PROGRAMMING SKILL IS REQUIRED*

Once the code is created you can edit manually and add/integrate your own features.

The final effect is awesome and the administrator feels like at home.
This is due to the windowed approach. Administrator already know how to handle a window, minimize, maximize, change wallpaper and themes etc.

It's a sort of *online MDI form Application Generator* which provides a simple way to create both the UI (User Interface) for the Frontend using kendo-ui framework and the Backend (*CRUD*) using Laravel framework.

Someone define it a sort of online access wizard, and it's not so far.

If you want to try out .... it's free
don't forget to star it if you like :)

- [Laravel](https://laravel.com/docs/5.6).
- [Telerik Kendo UI for jQuery](https://www.progress.com/kendo-ui).
- [Project homepage](http://www.simonecosci.com/wms).

## Installation
Cloning the git
```
git clone https://github.com/simonecosci/wms.git <install-directory>
cd <install-directory>
composer install
npm install
```

Via Composer
```
composer create-project simonecosci/wms <install-directory>
cd <install-directory>
npm install
```
## Database
Creata a new database
```
mysql -uroot -p
mysql> create database yourDatabaseName;
mysql> quit;
```

Then `cp .env.example .env` and update your database creds.
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=yourDatabaseName
DB_USERNAME=root
DB_PASSWORD=root
```

Change (if you want) the initial credential by editing the file `/database/seeds/UsersTableSeeder.php` or use these:

```
email: admin@example.com
password: admin
```

run the migrations with seed
```
php artisan migrate:fresh --seed
```
You can now run the web server

```
php artisan serve
```

or configure a virtualhost in your web server config

```
<VirtualHost *:80>
	ServerName localhost
	DocumentRoot "/<install-directory>/public"
	<Directory  "/<install-directory>/public/">
		Options +Indexes +Includes +FollowSymLinks +MultiViews
		AllowOverride All
		Require local
	</Directory>
</VirtualHost>
```

Navigate http://localhost/ and login

You have to give *write* permission to the following folders while your app is in development 
- app/Models
- app/Http/Controllers/Admin
- resources/views/admin
- database/migrations
- public/app
```
chmod -R 777 app/Models
chmod -R 777 app/Http/Controllers/Admin
chmod -R 777 resources/views/admin
chmod -R 777 database/migrations
chmod -R 777 public/app
```


## To create your first window read the [Wiki](https://github.com/simonecosci/wms/wiki)

<p align="center"><img src="http://www.simonecosci.com/storage/app/media/SS-2.JPG"></p>

## Licenses

The Laravel framework and the WMS are open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

The Kendo-UI framework is commercial software licensed [https://www.telerik.com/purchase/license-agreement/kendo-ui](https://www.telerik.com/purchase/license-agreement/kendo-ui).

Using this software requires a commercial license of Kendo UI
