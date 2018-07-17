# webpack-demo
webpack demo tutorial

### in installation progress, I met some problems.Locally install webpack and webpack-cli is invalid. So I install webpack and webpack-cli golobally.
### set up webpack.config.js file, and run webpack -d --watch successfully.


# Attention:
  在配置css loader的时候style-loader要放在css-loader前面。。。。

# Some Notes:
  当在css中引入背景图片，如：url('../images/1.png)，或者通过import引入文件的时候，webpack在打包的时候会把它们当做一个模块（module）来引入。