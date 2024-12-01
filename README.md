# About this Boilerplate
## Windows or MAC/Linux
This boilerplate is using environment variables.  
The used variables is for the Windows OS if you're  
using MAC or Linux remove the %'s and add a $ in   
front of the variable name (I guess :)).

### Windows
* %USERPROFILE%
* %OneDrive%
* %npm_package_config_dist_dir%
* %npm_package_config_port_dev%
* %npm_package_config_port_dist%
* %npm_package_config_backup_path%
* %npm_package_name%
* %npm_package_version%
* %npm_config_build%

### MAC/Linux
* $HOME
* $OneDrive ?
* $npm_package_config_dist_dir
* $npm_package_config_port_dev
* $npm_package_config_port_dist
* $npm_package_config_backup_path
* $npm_package_name
* $npm_package_version
* $npm_config_build

## package.json
The package.json file has only the basic fields.

"name": "rename-the-app"   
"version": "1.0.0",  
"main": "app.js",  
"author": "Change the author name",  
"homepage": "https://youtube.ulisdevcorner.com/",

### License
**Generic Info**: https://choosealicense.com/  
**No License**: https://choosealicense.com/no-permission/

### Config Variables

"config" : {   
&nbsp;&nbsp; "dist_dir": "public",  
&nbsp;&nbsp; "port_dev": "2001",  
&nbsp;&nbsp; "port_dev": "3001",  
&nbsp;&nbsp; "backup_path": "Backup/UlisDevCorner"  
}

Change the fields or add whatever you need.

**More Info**  
https://docs.npmjs.com/files/package.json

### Build Number
A build number will be crated with the NPM package build-number-generator,  
and stored in a temporary config variable npm_config_build, what will be later removed.

#### Windows
`FOR /F "tokens=*" %g IN ('buildnumgen') do (npm config set build %g)`
#### Mac/Linux (Not Tested)
`FOR /F tokens=* g IN ('buildnumgen') do (npm config set build g)`

### NPM Packages
#### Install 
Install all packages globally, so you don't need to install each package for every project you're working on. As well, you're good to go for **every project** used packages.  

#### Install Global

`npm i -g browser-sync build-number-generator cpy-cli del-cli minify mkdirp node-7z-archive npm-run-all replace-in-files-cli sass`

#### Install Dev

`npm i -D browser-sync build-number-generator cpy-cli del-cli minify mkdirp node-7z-archive npm-run-all replace-in-files-cli sass`

#### BrowserSync
https://www.npmjs.com/package/browser-sync
Keep multiple browsers & devices in sync when building websites.

`npm i browser-sync`

#### Build Number Generator
https://www.npmjs.com/package/build-number-generator
Generates a build number to be appended to your product version number, which is unique for each build and which can be read "by a human" to learn about the build time. No need for maintaining the most recent build number in your sources, incrementing it during the build and committing & pushing the new one to your sources.

`npm i build-number-generator`

#### Cpy CLI
https://www.npmjs.com/package/cpy-cli
Copy files

`npm i cpy-cli`

#### Del CLI
https://www.npmjs.com/package/del-cli
Delete files and directories

`npm i del-cli`

#### Minify
https://www.npmjs.com/package/minify
Minify - a minifier of js, css, html and img files.

`npm i minify`

#### MkDirP
https://www.npmjs.com/package/mkdirp
Like mkdir -p, but in Node.js!

`npm i mkdirp`

#### node-7z-archive
https://www.npmjs.com/package/node-7z-archive
ESM front-end to 7-Zip, featuring alternative full 7z CLI tool, binaries for Linux, Windows, Mac OSX, seamlessly create 7zip SFX self extracting archives targeting different platforms.

`npm i node-7z-archive`

#### NPM Run All
https://www.npmjs.com/package/npm-run-all
A CLI tool to run multiple npm-scripts in parallel or sequential.

`npm i npm-run-all`

#### Replace in files CLI
https://www.npmjs.com/package/replace-in-files-cli
Replace matching strings and regexes in files

`npm i replace-in-files-cli`

#### Sass
https://www.npmjs.com/package/sass
A pure JavaScript implementation of Sass. Sass makes CSS fun again.

`npm i sass` 

### The scripts
#### Development
Run `run:devOnline` or `run:devOffline` to start BrowserSync and watch your scss files. Change only files in the `app/src` directory. 
To build the project run `build:project` or build and run for final testing run `run:dist`.

#### Production
Run `run:dist` to create a compressed css files, and add vendor prefixes to the styles.

#### Backup Your Project
To backup the whole project in a zip file run `backup:project`