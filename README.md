# Build an Ember.js Blog

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
```
C:\Users\ADMIN\AppData\Roaming\nvm\temp
```

## Set up ember-cli
```
D:\gtechsltn\Build-Ember-Blog> npm install -g ember-cli
```

## Creating components
```
D:\gtechsltn\Build-Ember-Blog> ember -v
ember-cli: 3.10.1
node: 12.22.9
os: win32 x64
```

## Creating a new application
```
```

## Creating components
```
ember g component <component-name>
```

## Using Ember’s router
```
ember g route <route-name>
```

## Configuring the output of Ember's router

### application.hbs
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

## Deploy Ember application to Heroku
+ https://github.com/heroku/heroku-buildpack-emberjs

### Easy ember app demo
+ https://www.youtube.com/watch?v=-Ury2S9Y-4Q&ab_channel=YoloBrolo

### Playing Around with Ember Fastboot
+ https://www.youtube.com/watch?v=eZ-BY_tL1G4&ab_channel=YoloBrolo

### Material Design Lite for Ember.js Apps
+ https://github.com/mike-north/ember-material-lite
+ https://github.com/gtechsltn/ember-material-lite
