# Tor Buildpack for Heroku

This buildpack sets up [Tor][1] for your app on Heroku.

> Tor is a program you can run on your computer that helps keep you safe on the Internet. It protects you by bouncing your communications around a distributed network of relays run by volunteers all around the world: it prevents somebody watching your Internet connection from learning what sites you visit, and it prevents the sites you visit from learning your physical location. This set of volunteer relays is called the Tor network.

## Setup

**NOTE:** Tor uses SOCKS-proxy and only works with SOCKS-supporting apps.

#### Create a new app with this buildpack

Create a new Heroku app with this buildpack (through the [Heroku CLI][2]):

```shell
heroku create --buildpack "https://github.com/yumyum-web/heroku-install-TOR.git"
```

#### Or, add this buildpack to an existing app

1] Create a Heroku app as normal with the usual buildpacks.

2] Then, add this buildpack in your app (through the [Heroku CLI][2]):

```shell
$ heroku buildpacks:add "https://github.com/yumyum-web/heroku-install-TOR.git"
```

## Variables

You can provide tor version as a env variable ([check this guide][3]):

* `TOR_VERSION`: The version of Tor to install (default: its latest version).

## Features

* Caches compilation
* Verifies integrity (confirm yourself; it's provided as is without any warranty)

[1]: https://www.torproject.org/
[2]: https://devcenter.heroku.com/articles/heroku-cli#getting-started
[3]: https://devcenter.heroku.com/articles/config-vars#using-the-heroku-dashboard
