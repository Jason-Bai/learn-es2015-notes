* 使用nvm进行node版本管理

```
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/<version number>/install.sh | bash
```

* 查看当前node支持哪些ES2015特性

```
node --v8-options | grep harmony

```

* 使用阮一峰的es-checker查看当前node版本支持ES2015的特性

```
npm install -g es-checker
es-checker
```

* 使用babel将ES2015代码转换成ESCMScript 5代码，保持兼容，使用babel需要在项目更目录下配置.babelrc，格式如下

```
{
  "presets": [],
  "plugins": []
}
```

presets标识转码规则集合，

* 命令行转码babel-cli

```
npm install --global babel-cli
```
babel-cli工具自带一个babel-node命令，提供一个支持ES6的REPL环境。它支持Node的REPL环境的所有功能，而且可以直接运行ES6代码。它和coffee的功能一样。

* babel-register只是个钩子，对require进来的文件转码，由于不是实时，适合开发。

* babel-core提供转码API, babel-polyfill提供最新的API。
