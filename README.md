# github-pages 发布

#### 操作步骤

由于使用webpack打包生成的目录是dist

```shell

 git add dist
 
 git commit -m "build dist"
 
 git subtree push --prefix=dist origin gh-pages

```

