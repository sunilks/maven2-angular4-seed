# maven2-angular4-seed
A maven 2 project for angular.io v4.1.3+ which can run npm &amp; ng that is natively installed

## Documentation
Needed a way to use the system available node, npm & mvn to install angular.io dependencies and create a JIT bundles and then using mvn pom to create a web container deployable WAR file. So here goes, hope this helps all those looking for such a solution!

## What's included? The bells & whistles...
- Created using angular-cli
- Uses system installed node & npm
- D3 (needs to be imported)
- Bootstrap 3 (js + css)
- Tether.js
- JQuery (needs to be imported)
- Angular Material enabled
- Latest versions of @angular (+4.1.3) and its dependencies
- mvn tasks to clean up & create (prod ready JIT) deployable war file

## Rules
- Global libs, scripts: use the scripts section in *.angular-cli.json*.
- Global styles:  use scripts section in *.angular-cli.json* or *src/styles.css*.
- Use *src/assets* folder for files that need to be copied as is.

## Usage as is
* Clone the project `git clone https://github.com/sunilks/maven2-angular4-seed.git`
* Navigate to **mvn2ng2** `cd mvn2ang2` 
* Run `mvn clean install`

## Usage in your project
Please follow these steps:
* Create parent project folder using angular-cli `ng new <basedir>`
* All necessary folder structure will be created, henceforth referred as **basedir**
* Replace following files within appropriate folders:
* *pom.xml*: add to **basedir**.
* *.angular-cli.json*: add to **basedir**.
* *style.css*: add to **basedir/src**. 
* *src/index.html*: change *basehref* to `/artifactId-version/` (*include the slashes*).
* Run `mvn clean install` to recompile 
* Installs the node dependencies and builds the project using JIT in prod mode.
* Creates built artifacts & files in **basedir/src/dist** folder.
* Copies artifacts & files from **basedir/src/dist** folder to WEB-INF in **basedir/target** folder.
* Builds the files into a deployable WAR file **artifactId-version.war** in **basedir/target** folder.
* Deploy **artifactId-version.war** to app/web servers (e.g., wildfly et al.).
* Access using the appropriate link: `[http://<server>:<port>/artifactId-version]http://<server>:<port>/artifactId-version`
* **Enjoy!**

## Folders
* **basedir**: folder that houses your project
* **basedir/target**: folder in basedir with generated war
* **basedir/src/**: folder in basedir with angular.io application, assets & configurations
* **basedir/dist/**: folder in basedir housing the files created post the build (JIT prod mode)

## Dependencies & Must-haves
* Ensure mvn, node & npm is installed - uses natively installed versions. (*won't download node or npm*)
* Ensure all dependencies are appropriately mentioned in `package.json` using save or save-dev

## To build this project:
* Run `$ mvn clean install`

## To clean this project:
* Run `$ mvn clean`
* It'll delete the *src/dist* and *target* folders
* Currently will not clean *node_modules*

## Issues, Contributing

Please post any issues on the [Github's Issue tracker](https://github.com/sunilks/maven2-angular4-seed/issues).

All [Pull requests](https://github.com/sunilks/maven2-angular4-seed/pulls) are welcome! 

You can find a full list of [contributors here](https://github.com/sunilks/maven2-angular4-seed/graphs/contributors).

## License

[MIT](LICENSE)
