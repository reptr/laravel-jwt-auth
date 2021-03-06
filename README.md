# Laravel_JWT_AUTH

## Table of Contents
- [Laravel_JWT_AUTH](#laravel_jwt_auth)
  - [Table of Contents](#table-of-contents)
  - [About](#about)
  - [Routes API](#routes-api)
  - [How to use](#how-to-use)
  - [Screenshoot](#screenshoot)
  - [License](#license)

## About
Simple Laravel JWT AUTH. build with Laravel 8, PHP 8, and MariaDB.

## Routes API

Route prefix is `auth`, for detail check at `routes/api.php`

| Method  | Endpoint               |
|---------|------------------------|
| POST    | /api/auth/register     |
| POST    | /api/auth/login        |
| GET     | /api/auth/user-profile |
| POST    | /api/auth/refresh      |
| POST    | /api/auth/logout       |

## How to use

1. Clone this project
```
git clone https://github.com/reptr/laravel-jwt-auth /direktori project(htdoc)
```

2. Create database 

3. *Edit* .env
```env
DB_DATABASE= (fill database)
DB_USERNAME= (fill username)
DB_PASSWORD= (fill password)
```

4. *Composer Install*
```sh
composer install
```

5. *Migrate database*
```sh
php artisan migrate
```

4. *Generate Key*
```sh
php artisan key:generate
```
5. *Generate Secret Key JWT*
```sh
php artisan jwt:secret
```
After generated, you can check this key inside the `.env` file

6. *Finally, Running app*
```sh
php artisan serve
```

## Screenshoot

1. User Registration

<img src="screenshoot/jwtAuthRegister.png">

2. Login

<img src="screenshoot/jwtAuthLogin.png">


3. User Profile

    Make sure `fill token` the header field `Authorization: Bearer Token`

<img src="screenshoot/jwtAuthUserProfile.png">


4. JWT Token Refresh

    Make sure `fill token` the header field `Authorization: Bearer Token`

<img src="screenshoot/jwtAuthRefresh.png">


5. Logout

    Make sure `fill token` the header field `Authorization: Bearer Token`

<img src="screenshoot/jwtAuthLogout.png">


## License

MIT License &copy; 2021
