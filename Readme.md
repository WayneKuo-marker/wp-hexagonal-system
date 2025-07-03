WordPress Hexagonal Architecture Example
A plugin example built in a hexagonal way. This architectural approach enables future improvements, such as migrating the codebase to a framework (Symfony, Laravel...) and implementing next-level patterns like Domain-Driven Design (DDD) or CQRS after migration.
It can also serve as a WordPress plugin boilerplate.

The purpose of this project is to demonstrate that hexagonal architecture can be applied in most environments — including WordPress — and that it simplifies testing, debugging, and modification in a clearer, more maintainable way, without unnecessary overengineering.

You can see the plugin on: WordPress Plugins directory

It lacks:
A Dependency Injector (dependencies are wired manually via a class that implements the PHP-FIG PSR-11 Container interface — although most modern frameworks have automatic dependency injection)

An Event Dispatcher (a class simulates it synchronously by implementing PHP-FIG PSR-14)

A Database Migration Manager to handle plugin database updates (a very simple migration tool is included instead)

But it has features like:
Docker-ready setup for running unit and acceptance tests inside a WordPress container

Codeception for automated testing

Standalone Selenium Chrome with VNC support to visually observe BDD acceptance tests in action

How to develop locally
Run:

go
Copy
Edit
make vendors
Then install the project folder inside a WordPress installation as a normal plugin.

Run Automated Tests
Run:

go
Copy
Edit
make up
to start the Docker testing environment, and then:

go
Copy
Edit
make unit
to run unit tests

go
Copy
Edit
make acceptance
to run acceptance tests
