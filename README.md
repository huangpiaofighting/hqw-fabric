# hqw-fabric

快速创建eslint、prettier配置
未来: 使用.hqw文件配置项目

- [hqw-fabric](#hqw-fabric)
  - [安装](#安装)
  - [例子](#例子)
    - [eslintrc](#eslintrc)
    - [prettierrc](#prettierrc)
  - [版本日志](#版本日志)

## 安装

yarn add hqw-fabric -D

## 例子

### eslintrc

创建.eslintrc.js

``` JS
const config = {
  extends: [require.resolve('hqw-fabric')],
};
module.exports = config;
```

### prettierrc

在 `package.json` 中添加 `"prettier": "hqw-fabric/.prettierrc.js"`

``` json
{
    "name": "test",
    "version": "1.0.0",
    "description": "",
    "main": "index.js",
    "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1"
    },
    "author": "",
    "prettier": "hqw-fabric/.prettierrc.js",
    "license": "ISC",
    "devDependencies": {
        "eslint": "^7.24.0",
        "hqw-fabric": "1.0.2"
    }
}
```

or

创建.prettierrc文件

``` json
"hqw-fabric/.prettierrc.js"
```

tips: 建议使用.prettierrc文件，暴露给外部

## 版本日志

* `1.0.0` 创建模型
* `1.0.1` 添加jsx
* `1.0.2` 添加prettierrc配置
* `1.0.3` 添加jsconfig.json参照
