# Build an Ember.js Blog

Ember.js Installation

https://www.geeksforgeeks.org/ember-js-installation/

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

```
C:\Users\ADMIN\AppData\Roaming\npm\
C:\Users\ADMIN\AppData\Roaming\nvm\temp\
D:\gtechsltn\Build-Ember-Blog\
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
git push
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
