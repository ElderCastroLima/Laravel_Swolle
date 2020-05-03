## Laravel and Swolle in docker container
- Requirements 
    - Docker
    - Composer 
    - Laravel >= 5.6

## How to configure
- Clone or Download this project
- Run command Composer create-project --prefer-dist laravel/laravel {name_folder_your_app} 
- Access folder {name_folder_your_app} 
- Run command composer require swooletw/laravel-swoole
- Add the Service Provider in config/app.php 
```
	'providers' => [
        ... 
        SwooleTW\Http\LaravelServiceProvider::class,
    ]
- Copy Dockerfile in Swoole folder to folder {name_folder_your_app} 
- Run command docker build -t {tag} . 
- Run command docker run --rm --name swoole -p 80:80 -d {tag}:latest
- Open your browser and access localhost:80

## Credits for docker image
- Zaher Ghaibeh
- https://www.codementor.io/@zaher/using-swoole-php-7-2-docker-image-l3b1seiad
