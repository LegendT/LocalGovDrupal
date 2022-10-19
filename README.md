# LocalGov Drupal Composer project template

A Composer-based installer for the LocalGov Drupal distribution.

User name: admin User password: 9znQEmjvpZ

Modules:
https://essexcc.ddev.site/admin/modules

Although the installation instructions only talk of lando for setting up a local development environment, it can just as easily be set up with DDEV.

Prerequistes:
DDEV installed on host
composer 2.x installed (once installed, it's best to use the composer installed in DDEV)

These steps have been proven to work for an initial setup:

- Create a directory for your project `mkdir mycouncil && cd mycouncil`
- `composer create-project localgovdrupal/localgov-project . --no-install`

  ddev config starts an interactive (three step) session:

- `Project name (localgov):` <- hit return or change the name

  The next step is Docroot Location (current directory):. Type web and hit return. When prompted that the directory doesn't exist choose yes.

  When prompted for type of project, type drupal9 and hit return.

- Type `ddev start`
- Type `ddev composer install`
- Type `ddev drush si localgov -y`

  Copy the password for the admin user which is presented to you.

- Type `ddev launch`

  Go to /user and login with admin:<password_from_step_6>
