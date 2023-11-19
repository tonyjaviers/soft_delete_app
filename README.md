Soft Delete App

This Ruby on Rails application implements a basic soft delete functionality for a model named Item. Soft deletes involve marking records as "deleted" without physically removing them from the database. This is commonly used to implement features such as a trash/recycle bin.

Setup
Ruby version
This application requires Ruby version 2.7.5. You can install it using a version manager like RVM or RBenv.

System dependencies
Make sure you have the necessary system dependencies installed. This may include database-related dependencies. You can refer to the Ruby on Rails documentation for detailed instructions.

Configuration
No special configuration is required for this application.

Database creation
Run the following commands to create the database:

rails db:create
rails db:migrate

Database initialization
No specific initialization steps are required.

Running the Test Suite
To run the RSpec test suite, use the following command:

bundle exec rspec

This will ensure that the soft delete functionality is working as expected.

Usage
The Item model includes methods for soft deletion and restoration:

soft_delete: Soft deletes an item by updating the deleted_at attribute with the current timestamp.
restore: Restores a soft-deleted item by setting the deleted_at attribute to nil.
A default scope is applied to the Item model to exclude "deleted" items from normal queries.

Services
No additional services are required for this application.
