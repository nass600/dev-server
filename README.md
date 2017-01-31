# Development Server

Ubuntu 14.04 LTS virtual environment for PHP apps via Vagrant and Ansible.

<br>

## Installed Software

| ![](docs/img/nginx.png) | ![](docs/img/postgresql.png) |
|:-----------------------:|:----------------------------:|
| Nginx                   | PostgreSQL                   |
| 1.4.6                   | 9.3.15                       |

| ![](docs/img/php.png) | ![](docs/img/composer.png) | ![](docs/img/robo.png) |
|:---------------------:|:--------------------------:|:----------------------:|
| PHP                   | Composer                   | Robo                   |
| 7.0.15                | 1.3.2                      | 1.0.5                  |

| ![](docs/img/nodejs.png) | ![](docs/img/grunt.png) | ![](docs/img/bower.png) |
|:------------------------:|:-----------------------:|:-----------------------:|
| NodeJS                   | Grunt                   | Bower                   |
| 0.12.0                   | 1.2.0                   | 1.8.0                   |


<br>

## Requirements

You must have installed the following tools first:


| ![](docs/img/vagrant.png)             | ![](docs/img/ansible.png)              |
|:-------------------------------------:|:--------------------------------------:|
| [Vagrant](https://www.vagrantup.com/) | [Ansible](http://www.ansible.com/home) |

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
