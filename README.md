# Build an Ember.js Blog

https://servicestack.net/posts/

## How to use this repo on Windows 11 (64-bit)?
+ Install Git for Windows, Node.js, NVM, Visual Studio Code, Google Chrome, Ember CLI
+ Run some the following commands as in a queue
```
git clone https://github.com/gtechsltn/Build-Ember-Blog.git
nvm install 12.22.9
nvm use 12.22.9
npm install -g ember-cli@3.10.1
cd Build-Ember-Blog\src
code .
```

Visual Studio Code: Open the terminal by selecting View > Terminal from the menu bar, or by pressing the **Ctrl+`** keyboard shortcut.

https://code.visualstudio.com/docs/terminal/getting-started

+ Run some the following commands as in a queue
```
npm install
ember s
F5
```
# Tech Stack

https://github.com/h5bp/html5-boilerplate/

https://www.npmjs.com/package/create-html5-boilerplate

https://github.com/h5bp/html5-boilerplate/blob/v4.3.0/

https://github.com/h5bp/html5-boilerplate/blob/v4.2.0/

https://gist.github.com/gtechsltn/c56de381dca4b366b4386826a655d705

https://medium.com/codebagng/working-with-html5-boilerplate-fca93b9b61e9

https://www.freecodecamp.org/news/basic-html5-template-boilerplate-code-example/

https://github.com/gtechsltn/ember-template-boilerplate

https://github.com/gtechsltn/ember-boilerplate-template

```
npx create-html5-boilerplate new-site
cd new-site
npm install
npm run start
```

+ Handlebars
+ jQuery v3.7.1
+ Boostrap v3.3.7
+ HTML5 Boilerplate v4.2.0

## Guidance for developers of develop an Ember.js application

Ember.js Installation

https://www.geeksforgeeks.org/ember-js-installation/

Ember.js Create Application

https://www.geeksforgeeks.org/ember-js-create-application/

How to display a list of items

https://guides.emberjs.com/v2.6.0/templates/displaying-a-list-of-items/

How to set up a Basic Ember.js app

https://www.freecodecamp.org/news/setting-up-a-basic-ember-js-app-c9323760c675/

```
1. Set up ember-cli
2. Create a new application
3. Use materalize-css for styling
4. Create components
5. Cover basic use of Ember's router
6. Explore the "each" helper for iterating over data
```
## Setup Node.js and NVM

### How to Install Node.js and npm on Windows
+ https://www.freecodecamp.org/news/how-to-install-node-js-and-npm-on-windows/
+ https://www.freecodecamp.org/news/how-to-install-node-js-and-npm-on-windows-2/

### Node Version Manager – NVM Install Guide
+ https://www.freecodecamp.org/news/node-version-manager-nvm-install-guide/
+ https://www.freecodecamp.org/news/nvm-for-windows-how-to-download-and-install-node-version-manager-in-windows-10/

### Source Folder (Directory)
```
C:\Users\ADMIN\AppData\Roaming\npm\
C:\Users\ADMIN\AppData\Roaming\npm-cache\
C:\Users\ADMIN\AppData\Roaming\nvm\temp\
C:\Program Files\Google\Chrome\Application\chrome.exe
D:\gtechsltn\Build-Ember-Blog\
D:\gtechsltn\Build-Ember-Blog\src\
```

```
node -v
npm -v
nvm -v
ember -v
dotnet --version
```

```
nvm -v
1.1.12

nvm install 12.22.9
Downloading node.js version 12.22.9 (64-bit)...
Complete

nvm use 12.22.9
Now using node v12.22.9 (64-bit)
```

## Setup Git and dotnet-cli
```
dotnet new gitignore --force
```

## Set up ember-cli (latest version)
```
npm install -g ember-cli
```

## Set up ember-cli (version 3.10.1)
```
npm install -g ember-cli@3.10.1
```

## Check ember version
```
ember -v
ember-cli: 3.10.1
node: 12.22.9
os: win32 x64
```

## Creating a new application
```
ember new Ember-Blog
cd Ember-Blog
ember serve
```

## Creating components
```
ember g component <component-name>
```

## Using Ember's router
```
ember g route <route-name>
```

## Configuring the output of Ember's router

### app/templates/application.hbs
```
{{#link-to 'videos'}}Videos{{/link-to}}
```

## Iterating Over Data Using the Each Helper
```
<div class="row">
    <div class="col s12 m6 l4">
        <div class="card-panel center-align">
            <div class="purple-text">
                <p>Title</p>
            </div>
            <div class="video-container">
                <iframe width="853" height="480" src="https://www.youtube.com/embed/peNV2yJRMLo?rel=0" frameborder="0" allowfullscreen></iframe>
            </div>
            <div class="purple-text"> With Taras Mankovski </div>
        </div>
    </div>
</div>
```

## Model
```
model() {
  return this.store.findAll('user');
}
```

## Model (Adding Catch Block for Returned Promise)
```
model() {
  let userPromise = this.store.findAll('user');
  userPromise.catch((error) => {
    // transition to another route and show some error notification saying your team is doing their best to fix the problem
  });
  return userPromise; 
}
```
## Run Ember application
```
cd Ember-Blog
ember serve

Running without permission to symlink will degrade build performance.

See http://ember-cli.com/user-guide/#windows for details.

Build successful (27691ms) – Serving on http://localhost:4200/

Slowest Nodes (totalTime >= 5%)                                 | Total (avg)
----------------------------------------------------------------+----------------
Babel: @ember/test-helpers (2)                                  | 6625ms (3312 ms)
Packaged Javascript (1)                                         | 5034ms
Application Dist (1)                                            | 4220ms
broccoli-persistent-filter:EslintValidationFilter (2)           | 2896ms (1448 ms)
Rollup (1)                                                      | 1522ms
```

## Test Ember application
```
ember test
```

## Deploy Ember application to Heroku
+ https://github.com/heroku/heroku-buildpack-emberjs

### Easy ember app demo
+ https://www.youtube.com/watch?v=-Ury2S9Y-4Q&ab_channel=YoloBrolo

### Playing Around with Ember Fastboot
+ https://www.youtube.com/watch?v=eZ-BY_tL1G4&ab_channel=YoloBrolo

### Material Design Lite for Ember.js Apps
+ https://github.com/mike-north/ember-material-lite
+ https://github.com/gtechsltn/ember-material-lite

# Git Submodules
```
git rm --cached Ember-Blog
commit -m "Removed submodule Ember-Blog"
```

```
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Ember-Blog/

nothing added to commit but untracked files present (use "git add" to track)
```

```
git push
```

```
warning: ----------------- SECURITY WARNING ----------------
warning: | TLS certificate verification has been disabled! |
warning: ---------------------------------------------------
warning: HTTPS connections may not be secure. See https://aka.ms/gcm/tlsverify for more information.
warning: ----------------- SECURITY WARNING ----------------
warning: | TLS certificate verification has been disabled! |
warning: ---------------------------------------------------
warning: HTTPS connections may not be secure. See https://aka.ms/gcm/tlsverify for more information.
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 20 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 246 bytes | 246.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/gtechsltn/Build-Ember-Blog/
   37c1dd3..29f855b  master -> master
```

# Setup Visual Studio Code
+ Copy all files from **Ember-Blog** folder to **src** folder
+ Remove submodules **Ember-Blog**
+ Install Visual Studio Code
+ Install Bower and Yarn
 
```
D:\gtechsltn\Build-Ember-Blog>cd src
D:\gtechsltn\Build-Ember-Blog\src>code .
D:\gtechsltn\Build-Ember-Blog\src>npm install bower
D:\gtechsltn\Build-Ember-Blog\src>npm install yarn
D:\gtechsltn\Build-Ember-Blog\src>bower install
D:\gtechsltn\Build-Ember-Blog\src>yarn install
D:\gtechsltn\Build-Ember-Blog\src>ember s
```

```
npm cache clear && bower cache clean
rm -rf node_modules bower_components
npm install && bower install
npm install && yarn install
```

```
D:\gtechsltn\Build-Ember-Blog\src>npm install
D:\gtechsltn\Build-Ember-Blog\src>ember s
```

```
Running without permission to symlink will degrade build performance.
See http://ember-cli.com/user-guide/#windows for details.
```

# Visual Studio Code Chrome Debugger disable web security (.vscode\launch.json)
```
{
  // Use IntelliSense to learn about possible attributes.
  // Hover to view descriptions of existing attributes.
  // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
  "version": "0.2.0",
  "configurations": [
    {
      "type": "chrome",
      "request": "launch",
      "name": "Launch Chrome against localhost",
      "url": "http://localhost:4200",
      "runtimeArgs": [
        "--disable-web-security",
        "--ignore-certificate-errors"
      ],
      "webRoot": "${workspaceFolder}"
    }
  ]
}
```

### Disable web security in Google Chrome
```
You are using an unsupported command-line flag: --disable-web-security. Stability and security will suffer
```

## Researching
```
/*!
 */
```

## FE and BE

![FE and BE](https://github.com/user-attachments/assets/3eb6b25b-f2bd-450d-ad13-2cb0e8f3ad49)

![FE and BE](https://qph.cf2.quoracdn.net/main-qimg-c29407c9bbba51cd668ee7df585128e8-pjlq)

## Printing

Modern framework to print the web correctly

https://github.com/BafS/Gutenberg

## HTML5 Boilerplate (H5BP) (h5bp) Build Tools

https://initializr.v1v2.io/

https://github.com/h5bp/html5-boilerplate

https://github.com/h5bp/ant-build-script

https://github.com/verekia/initializr

https://github.com/verekia/initializr-template/

https://github.com/verekia/initializr-website/

```
npm install --global generator-h5bp
npm install --global yo
yo h5bp
```

```
npm install --global generator-h5bp
npm install --global generator-mobile-boilerplate
npm install --global generator-server-configs
```

## Git Status
```
On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   package-lock.json
        modified:   package.json

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        ../Ember-Blog/
        .vscode/
        jsconfig.json

no changes added to commit (use "git add" and/or "git commit -a")
```

# Heroku (Salesforce)
```
npm i heroku-cli
```

Quick start guide to creating and deploying a web app

https://mariechatfield.com/tutorials/web-app/

+ Set up your development environment
+ Create a new Ember app using Ember CLI
+ Add more content to your Ember app
+ Create a server with Express
+ Add an interactive Ember route
+ Deploy to Heroku
