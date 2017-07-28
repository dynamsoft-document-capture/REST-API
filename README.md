# Dynamsoft OCR RESTful API
Use the module to invoke Dynamsoft OCR RESTful API.

## Getting Started
1. Createa a Dynamsoft account and generate the [API key](https://cloud.dynamsoft.com/ocr/ocr-api-key-settings.aspx).

    ![OCR API key](http://www.codepool.biz/wp-content/uploads/2017/07/ddc-api-key.PNG)
2. Initialize the module:

    ```javascript
    var DDC = require('ddc');
    var key = '' // get the API key from https://cloud.dynamsoft.com/ocr/ocr-api-key-settings.aspx
    var ddc = new DDC(key);
    ```
3. Call a method.

    ```javascript
    ddc.queryQuota(function (error, response, body) {
        if (!error && response.statusCode == 200) {
            console.log(body);
        }
    });
    ```

## API List
* queryQuota(function(error, response, body) {})
* queryDisk(function(error, response, body) {})
* uploadFile(fileName, filePath, function(error, response, body) {})
* doOCR(data, function(error, response, body) {})
    ```javascript
    {"list":[{"file_name":"1.jpg"},{"file_name":"2.jpg"}]} // data
    ```
* downloadFile(fileName, function(error, response, body) {})
* deleteFile(fileName, function(error, response, body) {})
* deleteMultiFiles(data, function(error, response, body) {})
    ```javascript
    {"list":[{"file_name":"1.jpg"},{"file_name":"2.jpg"}]} // data
    ```