<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>

# laravel-laradock-starter

`laravel-laradock-starter` is a project that's designed to get you up and running very quickly with a Dockerized Laravel 5.4 application. It includes [laradock](https://laradock.io) as a git submodule, and adds some basic configuration to get you started using MySQL, Redis, and Nginx.

For more information about using and configuring [laradock](https://laradock.io), see their documentation.

## Installation

1. (Optional) Fork this repository to your own GitHub account

2. Clone this repository to your local environment and change directories to be in the cloned repository's root

```bash
# If you opted to fork the repo, replace "AC-TimRourke" with your GitHub username
git clone git@github.com:AC-TimRourke/laravel-laradock-starter.git
cd laravel-laradock-starter
```

3. Fetch the git submodules - this will clone [laradock](https://laradock.io) so that you can run your new Laravel application in a Docker environment

```bash
git submodule init
git submodule update
```

4. Copy the file `laradock-env-example` into the `./laradock` folder created by fetching the submodule, and rename it to `.env`

```bash
cp ./laradock-env-example ./laradock/.env
```

5. Copy the file `./.env.example` to the file `./.env`

```bash
cp ./.env.example ./.env
```

6. Run `composer install` to install the PHP dependencies for this project

```bash
composer install
```

7. Change directories to be inside the laradock submodule

```bash
cd laradock
```

8. Spin up your environment, including each of the containers you need for your project (MySQL, Redis, and Nginx are available to you by default)

```bash
docker-compose up nginx mysql redis
```

9. Set your application's secret key

```bash
php artisan key:generate
```

10. Visit [localhost](http://localhost) and enjoy!

## Learning Laravel

Laravel has the most extensive and thorough documentation and video tutorial library of any modern web application framework. The [Laravel documentation](https://laravel.com/docs) is thorough, complete, and makes it a breeze to get started learning the framework.

If you're not in the mood to read, [Laracasts](https://laracasts.com) contains over 900 video tutorials on a range of topics including Laravel, modern PHP, unit testing, JavaScript, and more. Boost the skill level of yourself and your entire team by digging into our comprehensive video library.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).
