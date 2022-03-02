# E-Commerce_site

[![License: MIT](https://img.shields.io/apm/l/vim-mode?color=orange&style=for-the-badge.svg)](https://opensource.org/licenses/MIT)

## Table of contents
- [Description](#description)
- [Strategy](#strategy)
- [Usage](#usage)
- [License](#license)
- [Questions](#questions)

## Description
# What is the app for?
 Build the back end for an e-commerce site by modifying starter code. Configure a working Express.js API to use Sequelize to interact with a MySQL database.

```md
AS A manager at an internet retail company
I WANT a back end for my e-commerce website that uses the latest technologies
SO THAT my company can compete with other e-commerce companies
```

## Strategy 
| Steps | Instructions | 
| ------------- |:-------------:| 
| Installation Requirements: npm i inquirer, npm run seed, dotenv and MySQL | COMPLETED |
| Applying relevant files to gitignore | COMPLETED |
| WHEN I add my database name, MySQL username, and MySQL password to an environment variable file THEN I am able to connect to a database using Sequelize | COMPLETED | 
| WHEN I enter schema and seed commands THEN a development database is created and is seeded with test data | COMPLETED | 
| WHEN I enter the command to invoke the application THEN my server is started and the Sequelize models are synced to the MySQL database | COMPLETED | 
| WHEN I open API GET routes in Insomnia for categories, products, or tags THEN the data for each of these routes is displayed in a formatted JSON | COMPLETED | 
| WHEN I test API POST, PUT, and DELETE routes in Insomnia THEN I am able to successfully create, update, and delete data in my database  | COMPLETED | 

## Final Look
# Usage
<img src='./public/assets/images/noteTaker.gif' alt="EMS_mySQL" >

### Database Models

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

### Associations
Executing association methods on the Sequelize models to create the following relationships between them:

* `Product` belongs to `Category`, and `Category` has many `Product` models, as a category can have multiple products but a product can only belong to one category.

* `Product` belongs to many `Tag` models, and `Tag` belongs to many `Product` models. Allow products to have multiple tags and tags to have many products by using the `ProductTag` through model.

## License
This project is available under the MIT license. Visit [License: MIT](https://opensource.org/licenses/MIT) for full license text

## Contribute
To contribute to Team Profile Generator, clone this repo locally and commit your code on a separate branch.


## Contact
Git profile: https://github.com/liamok19
Email: liamokane19@gmail.com