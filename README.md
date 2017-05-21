# maven2-angular4-seed
Created a maven 2 project for angular.io v4.1.3+ which can run npm &amp; ng that is natively installed


D3 (needs to be imported)
Bootstrap 3 (js + css)
Tether.js
Jquery (needs to be imported)
Angular Material
Plus latest versions of @angular and its dependencies
created using ng new
Included with mvn task to create (prod ready JIT) deployable war file

ALL MUST follow these Rules:
Global libs, scripts: use the scripts section in .angular-cli.json
Global styles:  use scripts section in .angular-cli.json or src/styles.css
Use src/assets folder for files that need to be copied just as is.

mvn tasks - till we have configured global pom.xml, please follow these steps:
Create parent project folder for e.g., iemrdash (per the attached example) using ng new iemrdash
All necessary folder structure will be created, henceforth will be called basedir
Extract the attached zip and copy/replace in the new folder only the following files to appropriate folders:
pom.xml: extract from attached zip to basedir.
pom.xml: in new pom.xml change <artifactId> & <version> to appropriate value
.angular-cli.json: extract from attached zip to basedir
style.css: extract from attached zip to basedir/src 
src/index.html: change <basehref> to /artifactId-version/.
Run mvn clean install to recompile & create war file
target: folder in basedir will have the generated war
Deploy artifactId-version.war is deployed to wildfly.
Access using: [http://<server>:<port>/artifactId-version]http://<server>:<port>/artifactId-version
Ensure node & npm is installed - will use the native one (won't download node or npm)
Ensure all dependencies are appropriately mentioned in save or save-dev
Can also work standalone - unzip; cd to unzipped folder - run mvn clean install!

## To build this project:

Run `$ mvn clean install`

## Issues, Contributing

Please post any issues on the [Github's Issue tracker](https://github.com/eirslett/frontend-maven-plugin/issues). 
[Pull requests](https://github.com/eirslett/frontend-maven-plugin/pulls) are welcome! 
You can find a full list of [contributors here](https://github.com/eirslett/frontend-maven-plugin/graphs/contributors).

## License

[MIT](LICENSE)
