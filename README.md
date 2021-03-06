# npm Enterprise Installer

[![Build Status](https://travis-ci.org/npm/npme-installer.svg?branch=master)](https://travis-ci.org/npm/npme-installer)

One-step-installer for npm Enterprise.

## Quickstart

To get up and running as quickly as possible, [see the quickstart guide on the docs site](https://docs.npmjs.com/enterprise/intro).

## Supported Platforms

Modern versions of Ubuntu (12.04+), CentOS/RHEL (7+), Debian (7.7+)

## Prerequisites

You can find [detailed prerequisites](https://docs.npmjs.com/enterprise/requirements) on the docs site.

## Installing

* [Install Node.js via package manager](https://nodejs.org/en/download/package-manager/)
* Update npm via `sudo npm i -g npm@latest`
* Then install `npme`:

```shell
sudo npm install npme -g --unsafe
```

Once installation is complete visit __https://your-server-address:8800__ and bypass the security warning (you can provide your own certificate later to prevent this warning). You will be presented with a management UI which allows you to configure your npm Enterprise appliance.

You can find [installation details](https://docs.npmjs.com/enterprise/installation) on the docs site.

## Connecting to the Registry

By default the npm Enterprise registry will be available on __http://your-server-address:8080__.

Simply run:

```shell
npm login --scope=@my-company-name --registry=http://your-server-address:8080
```

And publish modules using the corresponding scope name:

```json
{
  "name": "@my-company-name/my-module",
  "repository": {
    "url": "git://github.mycompany.com/myco/mypackage.git"
  }
}
```

Details on [client configuration](https://docs.npmjs.com/enterprise/client-configuration) and [using npm Enterprise](https://docs.npmjs.com/enterprise/using-it) can be found on the docs site.

## Updating

Access your server via HTTPS on port 8800 and check for updates via
the management console.
