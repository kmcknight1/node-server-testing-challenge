###RESOURCE
What resource will be used to complete this project?

##Products
-id
-name
-price

##Endpoints
-POST to create a product
-should return a status code 201 & length of amount created

    -DELETE to delete a product
        -should return a status code of 200 & length of amount created - deleted


    ***DON'T FORGET TO ADD THE

      beforeEach(async () => {
        await db("products").truncate();
      });

    SO THE DATABASE IS CLEAR BEFORE EACH TEST

##Server
-test the server?

##Database
-create 2 databases, one for development and one for testing

##TO-DO
-npx jest --init
-edit package.json
-test script should be cross-env DB_ENV=testing jest --watch
-npx knex init

        module.exports = {
      development: {
        client: 'sqlite3',
        connection: {
          filename: './data/products.db3',
        },
        useNullAsDefault: true,
        migrations: {
          directory: './data/migrations',
        }
      },
      testing: {
        client: 'sqlite3',
        connection: {
          filename: './data/test.db3',
        },
        useNullAsDefault: true,
        migrations: {
          directory: './data/migrations',
        }
      },
    };
