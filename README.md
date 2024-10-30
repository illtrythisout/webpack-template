# A Basic Webpack Template
Things to be added and set up are described below. Have fun!

## Webpack Specific Setup
**Add images in HTML:**
Paste the following in the Terminal:
```
npm install --save-dev html-loader
```

Add the following object to the `modules.rules` array within `webpack.common.js`:
```
{
  test: /\.html$/i,
  loader: "html-loader",
},
```

**Add images with JavaScript:**
Add the following object to the `modules.rules` array within `webpack.common.js`:
```
{
  test: /\.(png|svg|jpg|jpeg|gif)$/i,
  type: "asset/resource",
},
```

**Load Fonts:**
Add the following object to the `modules.rules` array within `webpack.common.js`:
```
{
  test: /\.(woff|woff2|eot|ttf|otf)$/i,
  type: "asset/resource",
},
```

## Install ESLint
**Basic Installation:**
Paste the following in the Terminal:
```
npm install eslint --save-dev
./node_modules/.bin/eslint --init
```
> [!TIP]
> The questionnaire will let you chose the Airbnb style guide.
> You can read all the rules for the Airbnb style guide by going checking `./node_modules/eslint-config-airbnb-base/rules`

**Basic Setup:**
Add the following to the `scripts` object within `package.json`:
```
npm install eslint --save-dev
"lint": "./node_modules/.bin/eslint ./"
```

To turn off Airbnb bugging you about `console.log` statements, add the following to the `rules` object within `eslintrc.js`:
```
"no-console": "off"
```
> [!TIP]
> You can also override other rules by changing the `rules` object in within `eslintrc.js`.
> Check how to do this in the [eslint website](https://eslint.org/docs/latest/rules/)

**VSCode Setup:**
1. Once you have the eslint extension installed and go to settings ( `Cmd + ,` )
2. Go to Extensions > ESLint
3. Turn on "Eslint: Enable"
4. Turn on "Eslint: Auto Fix On Save"