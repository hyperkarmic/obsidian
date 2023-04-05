```terminal
npm install sequelize

```
After installation, you can incorporate it into your app by requiring it in your code and defining a new instance of Sequelize. You will also need to define a model, which is a representation of a table in Sequelize.

Here is an example of how to define a model for a table called "tableName":

```javascript
const Sequelize = require('sequelize');

const sequelize = new Sequelize('database', 'username', 'password', {
  host: 'localhost',
  dialect: 'mysql'
});

const tableName = sequelize.define('tableName', {
  Country: {
    type: Sequelize.STRING
  },
  PhoneCode: {
    type: Sequelize.INTEGER
  },
  Capital: {
    type: Sequelize.STRING
  },
  IndependenceYear: {
    type: Sequelize.INTEGER
  },
},
{
  freezeTableName: true // Model tableName will be the same as the model name instead of being pluralized
});

```

In this example, we define a model called "tableName" with four columns: "Country", "PhoneCode", "Capital", and "IndependenceYear". Each column is defined with a data type.

To sync the model with the database, you can use the `sync` method. You can also create a new record in the table using the `create` method:

```javascript
tableName.sync({force: true}).then(function() {
  // Table created
  return tableName.create({
    Country: 'Afghanistan',
    PhoneCode: 93,
    Capital: 'Kabul',
    IndependenceYear: 1919
  });
});

```

To query the table, you can use the `findAll` method with a `where` clause to filter the results:

```javascript
tableName.findAll({
  where: {
    IndependenceYear: { $gt: new Date().getFullYear() - 50}
  }
});

```

In this example, we are querying for all the records where the Independence Year was less than 50 years ago.

To order the results by descending Independence Years, and limit the results to just show 2 of the records, skipping the first two, you can use the `findAll` method with `offset`, `limit`, and `order` options:

```javascript
tableName.findAll({
  offset: 2,
  limit: 2,
  order: [[sequelize.col('IndependenceYear'), 'DESC']]
});

```

In this example, we are skipping the first two records, limiting the results to two records, and ordering by descending Independence Years.

If you need to make changes to an existing table with data in it, you can use Sequelize migrations. Sequelize migrations allow you to create, modify, and delete tables and columns in a database. You can learn more about Sequelize migrations in the Sequelize documentation: [http://docs.sequelizejs.com/en/latest/docs/migrations/](http://docs.sequelizejs.com/en/latest/docs/migrations/).

