# One Roof

[![GitHub contributors](https://img.shields.io/github/contributors/code4romania/war-support-un-acoperis.svg?style=for-the-badge)](https://github.com/code4romania/war-support-un-acoperis/graphs/contributors) [![GitHub last commit](https://img.shields.io/github/last-commit/code4romania/war-support-un-acoperis.svg?style=for-the-badge)](https://github.com/code4romania/war-support-un-acoperis/commits/master) [![License: MPL 2.0](https://img.shields.io/badge/license-MPL%202.0-brightgreen.svg?style=for-the-badge)](https://opensource.org/licenses/MPL-2.0)

[See the project live](https://unacoperis.ro/en)

A Roof is a solution for identifying accommodation spaces to help refugees who arrive in Romania and need help immediately. The platform can register legal and natural persons who can provide rooms or buildings for people living in shelters provided by the Romanian authorities. A Roof is a platform developed by Code for Romania and managed by the CNCCI, National Center for Command and Coordination of Interventions and partner organizations.

The platform registers requests for assistance from refugees or organizations that provide them with support in identifying verified accommodation in the territory, in order to reduce the risks that lurk to the vulnerable.

The One Roof Platform is a project developed by the Code for Romania association in partnership with the Romanian Government, the Department for Emergency Situations, the International Organisation for Migration (IOM), UNHCR, the National Red Cross Society, the Federation of Non-Governmental Social Services Organizations and the Good Morning Association. The efforts of the Code for Romania War Task Force are supported by ING Bank Romania.

[Contributing](#contributing) | [Built with](#built-with) | [Repos and projects](#repos-and-projects) | [Deployment](#deployment) | [Feedback](#feedback) | [License](#license) | [About Code4Ro](#about-code4ro)

## Contributing

This project is built by amazing civic technologists and great volunteers and you can be one of them! Here's a list of ways in [which you can contribute to this project](.github/CONTRIBUTING.md). If you want to make any change to this repository, please **make a fork first**.

If you see something that doesn't quite work the way you expect it to, open an Issue. Make sure to describe what you _expect to happen_ and _what is actually happening_ in detail.

If you would like to suggest new functionality, open an Issue and mark it as a **[Feature request]**. Please be specific about why you think this functionality will be of use. If you can, please include some visual description of what you would like the UI to look like, if you are suggesting new UI elements.

## Built With

[Laravel](https://laravel.com) & [Bootstrap](https://getbootstrap.com)

### Programming languages

-   [PHP](https://php.com)
-   JavaScript

### Frontend framework

-   jQuery
-   Bootstrap CSS

### Package managers

-   Composer
-   NPM

### Database technology & provider

Mysql

## Repos and projects

https://github.com/code4romania/war-support-un-acoperis

## Deployment

See instruction from this [wiki page](https://github.com/code4romania/war-support-un-acoperis/wiki/Local-Development-Environment) [not available]

[Docker](https://docs.docker.com/get-docker/) & [Docker-Compose](https://docs.docker.com/compose/install/) should be used on the development environment.

### MacOS & Linux

If running on Linux, make sure to give proper permissions to the storage folder

```shell
	chmod -R 777 storage/
```

Run `make install` to build, start containers and run migration

Some other useful make commands:

-   `make start` - start an already installed application
-   `make shell` - open an bash inside the php container
-   `make npm-watch` - start npm hot-reloading for js files

### Windows

You can install `make` on windows using [GNUWin32](http://gnuwin32.sourceforge.net/packages/make.htm) or you can use WSL(Windows Subsystem for Linux).
Afterward you can use all the commands from the MacOS & Linux section

The application can be installed without using `make` by running the following commands:

```shell
	cp .env.example .env
	docker-compose up -d
	docker-compose exec php sh -c 'composer install'
	docker-compose exec php sh -c 'php artisan migrate --seed'
```

Some other useful commands:

-   `docker-compose up -d` - start an already installed application
-   `docker-compose exec php bash` - open an bash inside the php container
-   `docker-compose run --rm nodejs sh -c 'npm run watch'` - start npm hot-reloading for js files

### Access

The main application can be accessed via http://localhost:80.

The CMS can be accessed via http://localhost:80/cms.

PhpMyAdmin can be accessed via http://localhost:8080.

If custom hosts are required in any way, you can add the following entries in your local hosts file and use them accordingly.

```bash
127.0.0.1  un-acoperis.local
```

## Feedback

-   Request a new feature on GitHub.
-   Vote for popular feature requests.
-   File a bug in GitHub Issues.
-   Email us with other feedback contact@commitglobal.org

## License

This project is licensed under the MPL 2.0 License - see the [LICENSE](LICENSE) file for details

## About Commit Global

The team behind Commit Global has a robust and celebrated track record in the tech for social good field since 2015. We have built the fastest growing organization in the space, Code for Romania and set it up as a model of good practices on how to design and build technology that helps at scale. Our tools have served governments, UN agencies and large and small CSOs during crisis and peace time. Most recently we have built, deployed and maintained a first of its kind humanitarian ecosystem in support of refugees fleeing from Ukraine, ensuring their safe and uninterrupted access to information, healthcare and services, while equipping NGOs with the tools they need to be more effective.

All throughout our activity we have been one of the champions of cooperation and co-creation in the the civic tech field, constantly investing efforts and resources in working with and supporting the work of similar organizations around the world. As part of these efforts we created, curated and hosted the largest civic tech strategic event in history, the 2018 Code for All Global Summit: a 4 days offline event where hundreds of delegates from all continents exchanged ideas and digital solutions for the benefit of humanity.

Find more details on https://www.commitglobal.org/en
