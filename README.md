# Development Server

Ubuntu 14.04 LTS virtual environment for PHP apps via Vagrant and Ansible.

<br>

## Installed Software

| ![](docs/img/php.png =100x100) |   |   |   |   |
|--------------------------------|---|---|---|---|
| PHP |   |   |   |   |
| 7.0 |   |   |   |   |
+ [Git](http://git-scm.com)
+ [Nginx](http://nginx.org/)
+ [PostgreSQL](https://www.postgresql.org/)
+ [PHP 7.0](http://php.net/)
+ [Composer](https://getcomposer.org/)
+ [Node.js](http://nodejs.org/)
+ [Bower](http://bower.io/)
+ [Grunt](http://gruntjs.com/)

<br>

## Requirements

You must have installed the following tools first:

+ [Vagrant](https://www.vagrantup.com/)
+ [Ansible](http://www.ansible.com/home)

<br>

## Usage

Download the vagrant machine, start it and you are ready to go:

```bash
git clone git@github.com:nass600/dev-server
cd dev-server
ansible-galaxy install -r requirements.yml --ignore-errors
vagrant up
```

<br>

## License

[MIT](/src/master/LICENSE)

<br>

## Author

Ignacio Velazquez Gomez - [http://ignaciovelazquez.es]()
