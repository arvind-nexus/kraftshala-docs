# Steps to setup class.kraftshala.com on local ( windows )

### Plateform requirements:

- **mongodb** version 3.4
- **xampp** with php version 5.6
- **Composer** (dependency manager for PHP)
- Set environment variables path accordingly

    * In user variable

    ```
    C:\Program Files\MongoDB\Server\3.4\bin
    C:\composer
    C:\xampp\php
    ```

    * In system variable

    ```
    C:\xampp\php
    C:\composer
    ```


1. Clone Repository

2. Run below commond in project folder

    ```
     git pull origin master
    ```
    > .env, php_mongo.dll and dumb.zip are needed for setup => put php_mongo.dll file in xampp\php\ext folder, .env file in project root directory 
    >  and extract dumb.zip in C:\Program Files\MongoDB\Server\3.4\bin folder

3. Run below command

    ```
     composer install
    ```

4. Now before running mongod commond in bin folder i.e. C:\Program Files\MongoDB\Server\3.4\bin make sure below points

    * mongod commond by default search for **data/db** folder in root directory, so make sure you have these folders if you wanted to run mongod in some other folder, then you have to give the path of that folder while running **mongod** command
    * for example if you want to run it in **data/db/3.4** then run below command in **C:\Program Files\MongoDB\Server\3.4\bin** 

        ```
        mongod --dbpath "C:\data\db\3.4"
        ```       
        otherwise
        ```
        mongod
        ```

5. Make sure database name in dump folder and in .env file should be same their could be spelling and lower and upper
    case issue, so both should be exact same

6. Now run php artisan server --port=8100



