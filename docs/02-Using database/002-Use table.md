# 2. Create Table

### 2.1 Create Table If Not Exists.
  Creating a new database starts with defining its name. The syntax is as follows:
```bash
db.table("your_table_name");
```
  The columns and their data types must then be defined. If the data type is not defined, the script will automatically give it a VARCHAR(255) value.
  NOTE: You do not need to create an 'ID' table, it will be created automatically with the autoincrament parameter.
  The final step in creating a table is to use the save() method.
  ```bash
db.save();
  ```
Done, you have created a table!

### 2.2 Create a table with a one-to-many relationship
  If you want to create a database with a relation, you must have at least one table already created in your database!
  The structure itself is not too different compared to the create method itself, just add the following method before save.
  The final step in creating a table is to use the save() method.
  ```bash
      db.oneToMany("current_column", "target_table", "target_column");
  ```
  Example of command structure:
  FOREIGN KEY(current_column) REFERENCES target_table(target_column)
  In summary, a relational table is created using the standard table creation (Section 2.1), but before the save() method, the oneToMany method must be used with appropriately defined parameters.
### 3. Alter Table
* Currently AlterTable only supports the ability to add a new column to an existing table.
  To add a new table, use the following syntax:
    ```bash
        db.addColumnTo("table");
    ```
  This method is responsible for defining the table to which a column is to be added.
  Further steps are similar to the createTable method, i.e. we add the column using addColumn(); and finally the save method should be called.
  Full syntax example for the addColumnTo method.
  ```bash
        db.addColumnTo("user");
        db.addColumn("email","VARCHAR(255) NOT NULL");
        db.addColumn("uniqueId", "TEXT");
        db.save();
    ```