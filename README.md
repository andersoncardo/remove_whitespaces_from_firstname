This is a brief guide on how to install the cardoso/module-customer-products package using Composer

## Prerequisites
Before starting the installation process, make sure you have the following prerequisites installed:

PHP version 7.3 or later
Composer

## Installation

Open your terminal or command prompt.

Navigate to your project's root directory.

Run the following command to install the package:

```bash
composer require  cardoso/module-customer-extension
```
## Configuration
After installing the package, you will need to enable it in your Magento 2 project by running the following command:
```bash
php bin/magento module:enable Cardoso_CustomerExtension
```
After enabling the module, you will need to run the following command to update your project's dependencies:
After installing the package, you will need to enable it in your Magento 2 project by running the following command:
```bash
php bin/magento setup:upgrade
```


## Usage
 Once a new
customer is being registered, the extension checks the First Name field. If the First
Name field has whitespaces, they must be removed, so the customer entity is saved
without whitespaces in the First Name property. All checks and modifications must be
performed on the server side.
Once the customer has been successfully registered, the extension should invoke the
following actions.

● Log customer data (current date and time, customer first name, customer last
name, customer email) to a separate log file in the var/log directory.

● Send an email with the customer data (customer first name, customer last name,
customer email) to the Customer Support email address configured in Magento.

## License

[MIT](https://choosealicense.com/licenses/mit/)