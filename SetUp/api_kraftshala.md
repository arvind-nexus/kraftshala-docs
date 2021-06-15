# Steps to setup api.kraftshala.com on local ( windows )

### Plateform requirements:

- **xampp** with php version 7.1.3
- **Composer** (dependency manager for PHP)
    >  latest version of composer (can update composer with command i.e. 'composer self-update')

- Set environment variables path accordingly



1. Clone Repository

2. Run below commond in project folder

    ```
     git pull origin master
    ```
    > .env, php_mongo.dll are needed for setup => put **php_mongo.dll** file in **xampp\php\ext** folder, **.env** file in project root directory 

    >  note:: it is better to borrow .env, package.json, composer.json and php_mongo.dll from developer.


3. Run below command

    ```
     composer install
    ```
    if facing any issues thatn run below command

    ```
     composer update --ignore-platform-reqs
    ```

    if still face issue like: 

    ```
        Illuminate\Foundation\ComposerScripts::postAutoloadDump
        PHP Fatal error:  Declaration of Illuminate\Container\Container::get($id) must be compatible with
        Psr\Container\ContainerInterface::get(string $id) in D:\class\xampp\htdocs\classApi 
        main\class_api\vendor\laravel\framework\src\Illuminate\Container\Container.php on line 15

        Fatal error: Declaration of Illuminate\Container\Container::get($id) must be compatible with 
        Psr\Container\ContainerInterface::get(string $id) in D:\class\xampp\htdocs\classApi 
        main\class_api\vendor\laravel\framework\src\Illuminate\Container\Container.php on line 15
    ```

    then add below line in require object in  **composer.json**

    ```
        "psr/container": "1.0.0",
    ```

    for reference: after adding above line require object will look like

    ```
        "require": {
        		"php": "^7.1.3",
                "psr/container": "1.0.0",
                "ext-curl": "*",
                "ext-json": "*",
                "ext-mongodb": "*",
                "aws/aws-sdk-php": "^3.132",
                ......
                }
    ```

    now run

    ```
     composer update --ignore-platform-reqs
    ```

4. If all works fine without any errors, then run following command 

    ```
        php artisan serve --port=8100
    ```



