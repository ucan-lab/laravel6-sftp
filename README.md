# laravel6-sftp

```
$ git clone git@github.com:ucan-lab/laravel6-sftp.git
$ cd laravel6-sftp
```

```
$ mkdir sftp-store
$ echo "hello" > sftp-store/world.txt
```

```
$ mkdir .ssh
$ ssh-keygen -t rsa -b 4096 -N "" -f .ssh/ssh_host_rsa_key
```

```
$ docker-compose up -d --build
$ docker-compose exec app composer install
$ docker-compose exec app cp .env.example .env
$ docker-compose exec app php artisan key:generate
```

```shell-session
$ docker-compose exec app php artisan tinker
>>> Storage::disk('sftp-disk')->get('world.txt');
=> "hello\n"
```
