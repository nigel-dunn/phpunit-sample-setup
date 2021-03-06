# PHPUnit Sample Test Setup

This contains an example project containing a single PHPUnit test. You can use this to check that you have a working environment for running PHPUnit tests. 

You can either install the software you require and run throught the commands on your machine. Or you can use a VM (the provisioning script is provided in this repo).


## Installing required software on your machine

You need to install the following:

- PHP 5.3 or higher
- Composer [Install instructions](https://getcomposer.org/doc/00-intro.md)

Once installed use composer to download the required dependencies:

```
cd sample-unit-test-project
composer install
```


Finally run PHPUnit:

```
./vendor/bin/phpunit 
```

You should see an output along the lines of:

```
PHPUnit 4.8.0 by Sebastian Bergmann and contributors.

.

Time: 3.55 seconds, Memory: 4.25MB

OK (1 test, 1 assertion)
```

The important bit is the `OK (1 test, 1 assertion)`. If you see that then you've installed everything correctly to run PHPUnit!


## Using a VM

You need to install [vagrant](https://www.vagrantup.com/) on your machine. 

The from this directory provision the VM and log in to it:

```
vagrant up
vagrant ssh
```

This will provision a VM running Ubuntu 15.10. It will install PHP 5.6 and composer. Finally it will run composer. 

Once logged into the VM run PHPUnit:

```
cd /vagrant/sample-unit-test-project
./vendor/bin/phpunit
```


You should see an output along the lines of:

```
PHPUnit 4.8.0 by Sebastian Bergmann and contributors.

.

Time: 3.55 seconds, Memory: 4.25MB

OK (1 test, 1 assertion)
```

The important bit is the `OK (1 test, 1 assertion)`. If you see that then you've installed everything correctly to run PHPUnit!


