# A toolkit for module's author to quickly add module into SimplCommerce
SimplCommerce is a platform based on modular architecture at https://github.com/simplcommerce/SimplCommerce. This project aiming to build a toolkit for module's authors can generate the skeleton of the project and integrate into SimplCommerce in one step.
## Simpl-CLI
Simpl-CLI would be installed into the development environment to generate skeleton of the module. Several commands to create the module for SimplCommerce:
### simpl init module_name
This command will generate a module that following the requirement of SimpleCommerce rules.  

The module will be created in the current directory and will be validating the relationship with others modules like `SimplCommerce.Infrastructure.csproj` and `SimplCommerce.Module.Core.csproj`
### simpl build
Performing the steps for packing the module includes of:
* Assets are concatenating for admin pages.
* Generate scripts for database
* Zipping module into a package
* Generate config files

### simpl deploy simplcommerce_path
The step to deploy the module into SimplCommerce at a specific path as below:
* Validate the existing of module file in current directory
* Extract and copy assets into SimplCommerce
* Adding assets for Admin
* Run scripts to create database migration.
## Docker Image
A docker image that consists of .netcore SDK, Node.js and PostgreSQL-client
