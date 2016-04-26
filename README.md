## Setup React Dev Env From Zero

### install dev dependencies

```shell
mkdir react-demo && cd react-demo
npm init #直接enter到结束
npm install react react-dom --save
npm install babel-loader babel-core babel-preset-es2015 babel-preset-react babel webpack webpack-dev-server --save
touch index.html App.js main.js webpack.config.js
```

### webpack.config.js Example

```javascript
module.exports = {
    entry: './main.js',
    output: {
        path: './',
        filename: 'index.js'
    },
    devServer: {
        inline: true,
        port: 8080
    },
    module: {
        loaders: [
            {
                test: /\.js$/,
                exclude: /node_modules/,
                loader: 'babel',
                query: {
                    presets: ['es2015','react']
                }
            }
        ]
    }
}
```

