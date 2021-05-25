# Steps to create a web build

1. Delete the existing **build folder. (www > js > build)**

2. Change the build version under
   * main index.html
   
    ```javascript
         <link rel="stylesheet" href="css/fonts.css?v=1.5.58" />
         <script type="text/javascript" src="js/index.js?v=1.5.58"></script>
         <script type="text/javascript" src="js/build/app.min.js?v=1.5.58"></script>
    ```
   * main version.json
   
    ```javascript
         {
          "version": "1.5.58"
         }
    ```   
    
3. Run the following command: (This will generate a new build folder with new compiled code under www > js)
    ```javascript
        npm run build-web
    ``` 
    
4. Then compress the www folder into a zip folder  

### For Linux users

Run the following commands:

```javascript
sudo scp -i learnkraftshalacom.pem www.zip centos@learn.kraftshala.com:
sudo ssh -i learnkraftshalacom.pem centos@learn.kraftshala.com 
```
To Gain root access:
```javascript
sudo -i
```


