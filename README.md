# A Basic Webpack Template


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

## Install ESLint:
**Basic Installation:**
Paste the following in the Terminal:
```
npm install eslint --save-dev
./node_modules/.bin/eslint --init
```
[!TIP]
The questionnaire will let you chose the Airbnb style guide.