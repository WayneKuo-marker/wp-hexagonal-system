WordPress Hexagonal Architecture Example
This is an example of a WordPress plugin built using Hexagonal Architecture (also known as Ports and Adapters).
This architecture simplifies future enhancements — such as migrating the codebase to a framework like Symfony or Laravel, or implementing more advanced patterns like Domain-Driven Design (DDD) or CQRS.

It serves as a WordPress plugin boilerplate, with a clear separation of concerns to make the code easier to test, debug, and extend — without overengineering.

👉 View the plugin on the WordPress Plugin Directory

🚫 What's Missing
This example intentionally avoids some advanced tooling to stay lightweight:

Dependency Injection Container
Dependencies are wired manually through a class that implements the PSR-11 container interface.
(Most modern frameworks use automatic dependency injection.)

Event Dispatcher
A synchronous, simplified dispatcher is included to simulate PSR-14 events.

Database Migration Manager
Only a very basic migration tool is included to handle database updates.

✅ Included Features
Despite its simplicity, the project offers useful modern tooling:

🐳 Docker-ready — Easily launch WordPress for local testing (unit + acceptance)

🔁 Codeception — Pre-configured for automated test workflows

👀 Selenium Chrome with VNC — Visually observe BDD acceptance tests running in real time

🛠️ Local Development
To set up the plugin for local development:

Install dependencies:

bash
Copy
Edit
make vendors
Copy this project into the wp-content/plugins/ directory of your WordPress setup.

Activate the plugin via the WordPress admin panel.

🧪 Running Automated Tests
Start the testing environment:

bash
Copy
Edit
make up
Run unit tests:

bash
Copy
Edit
make unit
Run acceptance (BDD) tests:

bash
Copy
Edit
make acceptance
update readme
