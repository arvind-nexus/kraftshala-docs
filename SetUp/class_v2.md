
# Steps to setup class_v2 Plateform (APP) on local ( windows )

### Plateform requirements:

- **git** for version control system
- **nodejs** for packege management
- **cordova** to support android plateform


1. Clone Repository

2. Run below commond in project folder

    ```
     git pull origin master
    ```
    > It is better to borrow package.json, config.xml and .gitignore files from developer to reduce setup issues


3. get cordova-plugin-inappbrowser zip file from developer or just clone below git repository in the root folder

    ```
        https://github.com/apache/cordova-plugin-inappbrowser
    ```

    repeat same step as above for cordova-plugin-facebook4

    now make sure your folder structure should be look like below example folder 

    ```
        >class_v2 
        >cordova-plugin-inappbrowser    
        >cordova-plugin-facebook4 
    ```
      

3. Now run below command in project directory

    ```
     npm install
    ```
    
    if above command does not run successfully then run

    ```
        npm install --force
    ```
    if again it shows error related to sass while running above command  then run
    ```
        npm rebuild node-sass
    ```

4. Install cordava globally 

    ```
        npm install -g cordova
    ```
    and run 

    ```
       cordova platform add android 
    ```

    if it show error like 'script is disable' then go to **C:\Users\your_system_directory\AppData\Roaming\npm** and **delete .ps1** file and then again run above command

5. Now run below two cammands in different terminal to run the project in local

    ```
        npm start
        npm run watch

    ```
