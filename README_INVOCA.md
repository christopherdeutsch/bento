# README_INVOCA

This fork of Chef's bento adds customizations for use at Invoca. We use them to speed up
our test-kitchen workflow using Berkshelf, chef-zero, bento, packer, and Vagrant.

## Features

* Uses chef-zero
* Works with encrypted data bags
* Install specific chef versions via chef_dir variable

## Limitations

* Only supports Ubuntu amd64 Virtualbox Vagrants

## Installing cookbooks

We run `berks vendor` from our `revops-common` cookbook to vendor all cookbooks
we'll need for the chef-zero run. The ubuntu-14.04-amd64.json template sets
them up to be copied into /tmp.
