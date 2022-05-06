# e-commerce-back-end

## Description
This application showcases what the back-end of an e-commerce site should operate as. Within this application, the NPM packages, Express.js, Sequelize, and MySql2 are used in tandem to perform RESTful api methods so that users can access the database. 

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)
- [Tests](#tests)
- [Questions](#questions)


## Installation <a name="installation"></a>
This application requires Node.js, Express, Sequelize, MySql2, and dotenv to be installed before running. This can be resolved by inputting "npm i" in a command-line application. 


## Usage Information <a name="usage"></a>
This application allows users the capability of viewing, adding, editing, and deleting of categories, products, and tags.
To run the application after all has been installed, MySql can be accessed via the command line application by the command "mysql -u root -p". Afterwards, enter the password provided in the .env file. While MySql is running, make sure that it is placed in the root directory of the application before inputting the command "SOURCE db/schema.sql". MySql can be exited out of at this point with the command "\q" or "quit". The command "npm run seed" should be run next, followed by "npm start" to start the server to connect to the database. 

### Database Models

The database contains the following four models:

* `Category`

  * `id`

    * Integer.
  
    * Doesn't allow null values.
  
    * Set as primary key.
  
    * Uses auto increment.

  * `category_name`
  
    * String.
  
    * Doesn't allow null values.

* `Product`

  * `id`
  
    * Integer.
  
    * Doesn't allow null values.
  
    * Set as primary key.
  
    * Uses auto increment.

  * `product_name`
  
    * String.
  
    * Doesn't allow null values.

  * `price`
  
    * Decimal.
  
    * Doesn't allow null values.
  
    * Validates that the value is a decimal.

  * `stock`
  
    * Integer.
  
    * Doesn't allow null values.
  
    * Set a default value of `10`.
  
    * Validates that the value is numeric.

  * `category_id`
  
    * Integer.
  
    * References the `Category` model's `id`.

* `Tag`

  * `id`
  
    * Integer.
  
    * Doesn't allow null values.
  
    * Set as primary key.
  
    * Uses auto increment.

  * `tag_name`
  
    * String.

* `ProductTag`

  * `id`

    * Integer.

    * Doesn't allow null values.

    * Set as primary key.

    * Uses auto increment.

  * `product_id`

    * Integer.

    * References the `Product` model's `id`.

  * `tag_id`

    * Integer.

    * References the `Tag` model's `id`.

## License <a name="license"></a>
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Tests <a name="tests"></a>
Please update tests when appropriate and necessary.

## Questions <a name="questions"></a>
If there are any questions or concerns about the application, here is a link to my GitHub profile:

-JTreezy([github.com/JTreezy](github.com/JTreezy))

If there are any additional questions, here is my e-mail address to reach me.

-digitalsigna@gmail.com

# Submission
* GitHub: https://github.com/JTreezy/employee-management-system
* Walkthrough Video: https://drive.google.com/file/d/1lTnUM8ed6oO65L5ljEoYI_glDYUmM2SD/view