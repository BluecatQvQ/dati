# dati

## Vue-cli3 \+ pug \+ stylus

### pug及stylus的使用百度

### Vue-cli3中使用pug步骤

+ `npm i -D pug pug-html-loader pug-plain-loader`

+ i 为install的简写，-D为 --save-dev的简写（这样安装的包的名称及版本号就会存在package.json的devDependencies这个里面），-S为--save的简写（会将包的名称及版本号放在dependencies里面），-g为全局

+ 用npm i安装的模块无法用npm uninstall删除，用npm uninstall i才卸载掉

+ devDependencies  和 dependencies 的区别：devDependencies  里面的插件只用于开发环境，不用于生产环境，而 dependencies  是需要发布到生产环境

+ 根目录下新建vue.config.js文件并添加以下代码

    ```javascript
    module.exports = {
    chainWebpack: config => {
        config.module.rule('pug')
            .test(/\.pug$/)
            .use('pug-html-loader')
            .loader('pug-html-loader')
            .end()
        }
    }
    ```

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
