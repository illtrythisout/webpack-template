# A Basic Webpack Template:

## Add images in HTML:
**Paste the following in the Terminal:**
```
npm install --save-dev html-loader
```

**Add the following object to the** `modules.rules` **array within** `webpack.common.js`**:**
```
{
  test: /\.html$/i,
  loader: "html-loader",
},
```

## Add images with JavaScript:
**Add the following object to the** `modules.rules` **array within** `webpack.common.js`**:**
```
{
  test: /\.(png|svg|jpg|jpeg|gif)$/i,
  type: "asset/resource",
},
```

## Load Fonts:
**Add the following object to the** `modules.rules` **array within** `webpack.common.js`**:**
```
{
  test: /\.(woff|woff2|eot|ttf|otf)$/i,
  type: "asset/resource",
},
```