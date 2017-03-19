

ClientApp
    app                     // Angular2 app       
    dist
    boot-client.ts
    boot-server.ts
wwwroot
    dist
        mian-client.js      // compliation of angular2 app
        vendor.js           // compliation of all the third party libraries
        vendor.css          // compliation of all the third party css

appsettings.json            // asp.net core app settings 
webpack.config.js           // bundle  js and css file, const clientBundleOutputDir = './wwwroot/dist';
webpack.config.vendor.js
