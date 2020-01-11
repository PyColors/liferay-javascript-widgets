# Liferay JavaScript Widgets

To be able to load this project you must have all below:

## Java

## Liferay (7.2)

Follow those actions step by step [here](https://portal.liferay.dev/docs/7-1/deploy/-/knowledge_base/d/preparing-for-install)

## Run Liferay (7.2)

It would be always great idea to start Liferay server with **MySQL database**. You need to instruct Liferay to use MySQL instead of HSQLDB (default) database. For this, just create one file called **portal-ext.properties** just under the extracted folder of Liferay server.
Note: Liferay ships with default database called HSQLDB. It is embedded (in memory) database and no setup is required. However **Liferay does not recommend to use it in production environment**.

Make sure your have MySQL installed and running, create a database and then remplace: Database Name, username and, password within `portal-ext.properties` file.

- jdbc.default.url=jdbc:mysql://localhost:3306/**DATABASE_NAME**?useUnicode=true&characterEncoding=UTF-8&useFastDateParsing=false
- jdbc.default.username=**YOUR_USERNAME**
- jdbc.default.password=**YOUR_PASSWORD**

These are JDBC properties used by Liferay 7 to establish interaction with MySQL database.
Note: For Liferay 7, you need to install MySQL 5.7 or above.

## Create a JavaScript widget

Follow these steps to create your JavaScript Widget. Also, you will be able to create your JavaScript widget with:

- Angular Widget
- React Widget
- Vue.js Widget
- Metal.js Widget

Firstly, make sure you have Node.js. installed Note that Node Package Manager (npm) is installed with this as well. You’ll use npm to install the remaining dependencies and generator, and configure your npm environment.

Install Yeoman for the generator:
`npm install -g yeoman`

Install the Liferay JS Generator:
`npm install -g generator-liferay-js`

Run the generator with the command below, select the JavaScript widget you want to create, and answer the prompts that follow.
`yo liferay-js`

If you specified your app server information when your widget was generated, you can deploy your widget by running the command below. You can verify this by checking the value of the `liferayDir` entry in the widget’s `.npmbuildrc`

`npm run deploy`

## Test your widget

Run your Liferay at: http://localhost:8080 and drag and drop your JavaScript widget into the page.
