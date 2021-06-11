# Steps to setup Learn Plateform on local ( windows )

### Plateform requirements:

- **git** for version control system
- **nodejs** for packege management


1. Clone Repository

2. Run below commond in project folder

    ```
     git pull origin master
    ```
    > It is better to borrow env.json,package.json and .gitignore files from developer to reduce setup issues

3. Run below command in project directory

    ```
     npm install
    ```

4. If step 3 shows some errors like:
    ```
     gyp ERR! find Python 
     gyp ERR! find Python Python is not set from command line or npm configuration
     gyp ERR! find Python Python is not set from environment variable PYTHON
    ```
    then run following command in cmd (run cmd as administrator)

    ```
        npm install --global --production windows-build-tools
        npm install node-gyp
    ```
        
    Ignore wornings while installation

    - if errors continues then run below command
    
    ``` 
        npm install --force
    ```

5. Now run below cammands to run the project in local

    ```
        now run: npm start
        npm run watch

    ```

    now if it shows packages not found in console or teminal then install those package seperately
    for example:
        ```
        npm rebuild node-sass
        npm install react-spring
        npm i @react-pdf/renderer
        ```
        and install all the packages seperately which shows not found errors...

