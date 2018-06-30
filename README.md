# Vagrant Dev Server

Ubuntu 16.04.03 LTS virtual environment for PHP apps via Vagrant and Ansible.

<br>

## Installed Software

|                              | name       | version       |
|:----------------------------:|:----------:|:-------------:|
| ![](docs/img/ubuntu.png)     | Ubuntu     | `16.04.3 LTS` |
| ![](docs/img/git.png)        | Git        | `2.11.0`      |
| ![](docs/img/nginx.png)      | Nginx      | `1.4.6`       |
| ![](docs/img/postgresql.png) | PostgreSQL | `9.3`         |
| ![](docs/img/mongodb.png)    | MongoDB    | `3.2.19`      |
| ![](docs/img/mysql.png)      | MySQL      | `5.7.22`      |
| ![](docs/img/php.png)        | PHP        | `7.2`         |
| ![](docs/img/composer.png)   | Composer   | `1.3.2`       |
| ![](docs/img/robo.png)       | Robo       | `1.0.5`       |
| ![](docs/img/nodejs.png)     | NodeJS     | `8.9.4`       |

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
