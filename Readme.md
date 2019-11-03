# Trillo

## Summary
Trillo is a fictional all in one booking app. The idea is that an user can book a hotel, a flight, a car, and a tour all in one platform. There's no functionality, we are going to code the User Interface.

### Automatic reload web browser
- `sudo npm i live-server -g`
- `live-server` in the main folder

## Dev Dependencies
- `npm i node-sass --save-dev`
- `npm i concat --save-dev`
- `npm i autoprefixer --save-dev`
  - `npm i postcss-cli --save-dev`
- `npm i npm-run-all --save-dev`

## Script
```

"scripts": {
    "watch:sass": "node-sass sass/main.scss css/style.css -w",
    "devserver": "live-server",
    "start": "npm-run-all --parallel devserver watch:sass",
    "compile:sass": "node-sass sass/main.scss css/style.comp.css",
    "concat:css": "concat -o css/style.concat.css css/icon-font.css css/style.comp.css",
    "prefix:css": "postcss --use autoprefixer -b 'last 10 versions' css/style.concat.css -o css/style.prefix.css",
    "compress:css": "node-sass css/style.prefix.css css/style.css --output-style compressed",
    "build:css": "npm-run-all compile:sass concat:css prefix:css compress:css"
  },

```

### Resources
- https://icomoon.io/


## Check it out
[Trillo](https://araqueheinz.github.io/Project-Trillo/)
