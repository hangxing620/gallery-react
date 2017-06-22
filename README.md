# github-pages 发布

#### 操作步骤

由于使用webpack打包生成的目录是dist

```shell

 git add dist
 
 git commit -m "build dist"
 
 git subtree push --prefix=dist origin gh-pages

```

#### bug部分

由于生成的index.html里面的
```javascript

# 原来生成的js
<script type="text/javascript" src="/assets/app.js"></script>

# 修改后的js
<script type="text/javascript" src="./assets/app.js"></script>
```

打包后的image图片地址有问题，需修改publicPath的路径。
```javascript

# old cfg/default.js 
module.exports = {
  srcPath: srcPath,
  publicPath: '/assets/',
  port: dfltPort,
  getDefaultModules: getDefaultModules
};

# new cfg/default.js
module.exports = {
  srcPath: srcPath,
  publicPath: './assets/',
  port: dfltPort,
  getDefaultModules: getDefaultModules
};

```



