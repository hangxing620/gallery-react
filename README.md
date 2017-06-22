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



