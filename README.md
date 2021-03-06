Sprint Board
-------------------

This is a simple angular-based, single-page app used for sprint planning that interacts with third-party task providers (e.g. Asana). It may be of interest if your team uses a points system to do time estimations for tasks.

Features
===========

 - Assign and remove points for tasks
 - View tasks for other sprint projects

Supported Task Providers
=========================

A task provider is defined here as a third-party service that manages task lists.

 - [Asana](https://asana.com)

Requirements
==================

Install node and npm.

    sudo pacman -S nodejs

Then `cd` to the board directory and run

    npm install

This will install the packages from `packages.json`.

Then install `grunt` and `bower` as root.

    sudo npm install -g grunt-cli bower

Install `bower` packages:

    bower install

Then build the app with `grunt`:

    grunt build

Finally, run the server:

    grunt serve

Compass
===========

If using `rbenv` to manage rubies, you'll need to set the global ruby to the `rbenv` installed one:

    rbenv global 2.1.1

Then reload `rbenv`:

    rbenv rehash

Check where `ruby` is pointing to (it should be something like this):

    $HOME/.rbenv/shims/ruby

Then install the `compass` gem:

    gem install compass
    rbenv rehash

Make sure the command `compass` is found:

    compass -v

Setup
===================

Create a `config.js` based on `app/scripts/config.js.example`.

You will need to obtain an API Key for Asana as documented [here](http://developer.asana.com/documentation/#api_keys) and figure out the `WORKSPACE_ID` and `PROJECT_ID` from the `https://app.asana.com/<workspace-id>` url.
