# Wordpress hexagonal architecture example

A plugin example created in an hexagonal way. That way of work facilitates future improvements like migrate the code to 
a framework (symfony, laravel...) and next iterations once is migrated like Domain Driven Design (DDD) or CQRS. It can be
used as a wordpress plugin boilerplate.

The purpose of this project is to demonstrate the hexagonal architecture is able to be implemented in most of the places and
facilitates testing, debugging and modification in a more visible way, like a wordpress plugin can provide, without overenginering inside it.

You can see the plugin on: [WordPress Plugins directory](https://wordpress.org/plugins/hexagonal-reviews/)

## It has features like:

* Docker ready for launching unit and acceptance tests on a wordpress container
* Codeception for automated testing
* Standalone selenium chrome with vnc capabilities to see what the BDD acceptance tests are doing

## How to develop locally

Run: 
make vendors
 and then

Install the project folder inside a wordpress like a normal plugin

### Run Automated Tests

Run: 
make up
 to start docker testing environment and then:

make unit
 to run unit tests

make acceptance
 to run acceptance tests
