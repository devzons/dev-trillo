# dev-trillo
# Node SASS

- install node-sass, live-server -g

```
# script - keep watching ('-w')
"compile:sass": "node-sass sass/main.scss css/style.css -w"

# run from CLI
live-server
npm run compile:sass
```

# Flexbox

| CONTAINER                                                                               | ITEM                                                             |
| --------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| 1. flex-direction: row /row-reverse/column/column-reverse                               | 1. align-self: auto /stretch/flex-start/flex-end/center/baseline |
| 2. flex-wrap: nowrap /wrap/wrap-reverse                                                 | 2. order: 0                                                      |
| 3. justify-content: flex-start /flex-end/center/space-between/space-around/space-evenly | 3. flex-grow: 0                                                  |
| 4. align-items: strech /flext-start/flex-end/center/baseline                            | 4. flex-shrink: 1                                                |
| 5. align-content: stretch /flex-start/flex-end/center/space-between/space-around        | 5. flex-basis: auto                                              |

### Trillo project

- install auto-prefixer, concat, node-sass, npm-run-all, postcss-cli
- package.json

```
   "watch:sass": "node-sass sass/main.scss css/style.css -w",
    "devserver": "live-server",
    "start": "npm-run-all --parallel devserver watch:sass",
    "compile:sass": "node-sass sass/main.scss css/style.css",
    "prefix:css": "postcss --use autoprefixer -b 'last 10 versions' css/style.comp.css -0 css/style.perfix.css",
    "compress:css": "node-sass css/style.prefix.css css/style.css --output-style compressed",
    "build.css": "npm-run-all compile:sass prefix:css compress:css"
  },

  npm run start
```

### Build project

```
npm run build:css

npm run deploy
```

### check live

[https://devzons.github.io/dev-trillo](https://devzons.github.io/dev-trillo)

### Amazon color

```
// $color-darkblue: #131a21;
// $color-midblue: #22303e;
// $color-orange: #f3a746;
// $color-background: #e9eded;
// $color-lightblue: #485868;
```
