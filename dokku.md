# Dokku

## Application

### New application

```sh
dokku apps:create my-super-app
```

### Deployment

In local machine

```sh
git remote add dokku dokku@dokku.me:my-super-app
git push dokku master
```

or if you want to deploy another branch

```sh
git push dokku another-branch:master
```

### Logs

```sh
dokku logs my-super-app
```

### Rebuild

```sh
dokku ps:rebuild my-super-app
```

### Start

```sh
dokku ps:start my-super-app
```

### Stop

```sh
dokku ps:stop my-super-app
```

### Remove

```sh
dokku apps:destroy my-super-app
```

### Rename

```sh
dokku apps:rename my-super-app my-stupid-app
```

### Set environment variables

```sh
dokku config:set my-super-app ENV=prod COMPILE_ASSETS=1
```

## Plugins

### Install plugin

Dokku's official plugins > [Official plugins](http://dokku.viewdocs.io/dokku/community/plugins/#official-plugins-beta)

```sh
sudo dokku plugin:install https://github.com/dokku/dokku-postgres.git
```

### Create plugin service

```sh
dokku postgres:create rails-database
```

### Link plugin to application

```sh
dokku postgres:link rails-database my-super-app
```

## Domains

## Let's encrypt Plugin

### Installation

```sh
sudo dokku plugin:install https://github.com/dokku/dokku-letsencrypt.git
```

### Enable / Renew encryption

```sh
sudo dokku letsencrypt <app>
```

### Auto renew

```sh
sudo dokku letsencrypt:auto-renew <app>
```

## Backups

```sh
dokku postgres:export [db_name] > [db_name].dump
dokku postgres:import [db_name] < [db_name].dump
```
