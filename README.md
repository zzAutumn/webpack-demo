# webpack-demo
webpack demo tutorial

### in installation progress, I met some problems.Locally install webpack and webpack-cli is invalid. So I install webpack and webpack-cli golobally.
### set up webpack.config.js file, and run webpack -d --watch successfully.


# Attention:
  在配置css loader的时候style-loader要放在css-loader前面。。。。

# Some Notes:
  当在css中引入背景图片，如：url('../images/1.png)，或者通过import引入文件的时候，webpack在打包的时候会把它们当做一个模块（module）来引入。这个时候就要用到file-loader，简单一点来说（不严谨）它可以把你src下的图片复制你打包出口的目录，这样css中的图片url也相对的改变了，所以能够正确引用图片。

  在file-loader中的设置：
  ```
  options: {
         name: '/images/[name]-[hash:5].[ext]',
        }
  ```
  这句配置的意思是打包的时候会在dist目录下生成一个images目录，在该目录下生成的图片名称是原名称-5个哈希数.扩展名。然后这样配置了也会找不到图片，
  在output中的设置：
  ```
  output: {
    filename: 'bundle.js',
    path: __dirname + '/dist',
    publicPath: 'dist'
  },
  ```
  重点是publicPath指向'dist'，这样就能正确找到图片了。
