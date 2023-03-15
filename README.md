# cost-finder
A web application which shows cost explorer to view different types of costs for various projects that your company is working on for multiple clients.


Installation and Contribution
Requirements :
PHP >= 7.1
MySQL >= 5.7
Composer
Laravel == 5.7.*
Completed Tasks :
[x] Set up the database structure.
[x] Populate the database using the SQL dump given in this file through Laravel Database Seeding
[x] Create an endpoint which returns this cost data in the JSON structure given here, by fetching the data from the database.
Bonus Tasks :
[x] Add ability to filter the cost data by Client(s), Project(s), and Cost Type(s).
Usage :
Endpoint: /cost-explorer
Output: Cost data of all clients and their projects

Endpoint: /cost-explorer?clients[]=1&clients[]=2
Output: Cost data of clients 1 and 2, and their projects

Endpoint: /cost-explorer?clients[]=1&clients[]=2&projects[]=1
Output: Cost data of project 1 for clients 1 and 2

Endpoint: /cost-explorer?cost_types[]=1&cost_types[]=2&cost_types[]=3
Output: Cost data with cost types 1, 2, and 3, for all clients (and their projects)

Project Setup :
Fork and Clone this repo or download it on your local system.

Open composer and run this given command.

composer install
composer update
After installing composer, Rename the file .env.example to .env.

cp .env.example .env
> Set db credentials in .env and run the following Commands.

Generate the Application key

php artisan key:generate
Migrate the database.

php artisan migrate
php artisan db:seed
> Run this project on localhost

php artisan serve
This project will run on this server:

http://localhost:8000/
