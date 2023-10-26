# 1. Connect to database

### 1.1. Define driver
  To connect to the database, declare the variable 'db' as follows.
  ```bash
  db<-DatabaseEngineController("YOUR DB DRIVER");
  ```
  You have a choice of two database drivers, you can enter "sql" or "mysql", enter one of these values.
  Jeżeli chcesz utworzyć własny driver to:

  **tutaj jakies info o tym kiedys.**

### 1.2. Connect to Database
  Hook "db" jest teraz reprezentowany jako obiekt. Każde kolejne działanie będzie się odbywało na zasadzie OOP.
  W celu uzyskania połączenia wykonaj następujące polecenie
  ```bash
  db.connect("db_name"); //SQL.
  //or
  db.connect("db_name", "db_ip_address", "db_user_name", "db_user_password");//MYSQL
  ```
  Edit the following variables according to your database data.
    * db_name >> Name of the database.
    * db_ip_address >> IP address of the database server, not required in SQL type.
    * db_user_name >> database user name, not required in SQL type.
    * db_user_password >> password of the database user, not required in SQL type.
