# README_INVOCA

This fork of Chef's bento adds customizations for use at Invoca. We use them to speed up
our test-kitchen workflow using Berkshelf, chef-zero, bento, packer, and Vagrant.

## Features

* Uses chef-zero
* Works with encrypted data bags
* Install specific chef versions via chef_dir variable
* Only supports Ubuntu amd64 Virtualbox Vagrants (sorry)

## How it Works

Set the chef_install_cookbook_dir vaiable to the location of your cookbooks,
data_bags, environment, nodes, etc. directories. The chef_environment is set to
test by default.

In our workflow at Invoca, we run `berks vendor` from our `revops-common` base cookbook
to vendor all the cookbooks we'll need for the chef-zero run.
