## VS Code and extensions
* Add extensions

* Add code command to system

    shift + cmd + p
    
    Install ‘code’ command in PATH

## Yeoman
    $ npm install -g yo generator-aspnetcore-spa 

    $ yo aspnetcore-spa

## Docker
* Download image

    $ sudo docker pull microsoft/mssql-server-linux
* Run image

    $ sudo docker run -e ‘ACCEPT_EULA=Y’ -e ’SA_PASSWORD=xxxxxxxxxx’ -p 1433:1433 -v /user/my/db:/var/opt/mssql -d microsoft/mssql-server-linux
    
    -v /user/my/db:/var/opt/mssql doest work on Mac
* Copy sql server error log

    $ docker cp <container>:/var/opt/mssql/log/errorlog . 

## Webpack
* Compile third part js lib to /wwwroot/dist and ClientApp/dist
    
    $ webpack --config webpack.config.vendor.js

* Compile ts file to /wwwroot/dist

    $ webpack --config webpack.config.js
    