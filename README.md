Digital Polygon Drupal Recommended Project
====

This is an opinionated project template for new Drupal 9 projects. It is based on the [Drupal Recommended Project](https://github.com/drupal/recommended-project/tree/9.3.x), with the principal difference being the addition of several modules and themes.

## It includes
* Drupal Core
* [Drush](https://github.com/drush-ops/drush) (Drupal CLI and development tool)
* [DDev](https://ddev.readthedocs.io/)
* [Asset Packagist](https://asset-packagist.org/) repository, package, and configuration
* [GrumPHP](https://phpqa.io/projects/grumphp.html)

## Installation and usage
Create a new project using composer
```
composer create-project --no-interaction digitalpolygon/drupal-recommended-project
```

After creating the project, it can be completely customized to suite your requirements. You should never update the project template.

## Local Setup
Once you have the project dependencies setup on your local environment, you should be able to setup your local environment with the sites.
1. Create a composer project using
```
composer create-project --no-interaction digitalpolygon/drupal-recommended-project
```
2. Configure git by executing
    - git config user.email "user@example.com"
    - git config user.name "Your Name"
3. Move into the project folder - `cd drupal-recommended-project`
4. If you are using `Macbook M1` please proceed to [Configuring Project for Apple M](#configuring-project-for-apple-m1)
5. Run ```ddev setup``` to build your project locally
6. Your [local](https://drupal-recommended-project.ddev.site/) site should be up and running

### Configuring Project for Apple M1

#### 1. Update `.ddev/docker-compose.local.yaml`
Create the file if it doesn't already exist. Update it so that the `web` service has property `platform: linux/x86_64`. Example:
adfdsaf
```yaml
services:
  web:
    platform: linux/x86_64
```
#### 2. Update `.ddev/config.local.yaml`
Create the file if it doesn't already exist. Update it so `mutagen_enabled: true` is set.

### Useful ddev commands
1. `ddev setup` - Use this command to setup the project from scratch.
2. `ddev refresh` - Use this command to sync your local with dev environment.
3. `ddev xdebug on` - Use this command to enable xdebug.
