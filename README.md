# hexo-theme-jane

### 关于

这是一个极其简单的 hexo 主题，甚至说，她是不及格的。这完全是按照我自己的需求和想法来设计的一个主题，没有太多的功能，例如，没有搜索功能，没有海贼王和火影忍者，没有分享，也没有脸书和推特。因为，我只希望这仅仅是一个给自己记录文字的地方，所以，没有太多花俏的功能！

如果您也喜欢这样，欢迎您使用的我的主题！

### 安装

```bash
git clone https://github.com/hejianxian/hexo-theme-jane.git themes/jane
```

然后配置根目录的_config.yml文件（并非theme里的那个）

```bash
theme: jane
```

若要作为git子模块安装
```bash
git submodule add https://github.com/hejianxian/hexo-theme-jane.git themes/jane
```
[关于git子模块](https://yuguo.us/weblog/git-submodule/)

### 关于评论

新的 jane 主题使用了 [gitment](https://github.com/imsun/gitment) 评论系统，具体操作请看[这里](https://imsun.net/posts/gitment-introduction/)，若有任何问题，欢迎提 issue。

如果注册 OAuth App 成功后，需要修改主题文件，找到`layout/_partial/article.ejs`，拉到最底下：

```js
// 请在这里正确地设置信息
var gitment = new Gitment({
  owner: '你的 github account',
  repo: '接收 issue 的仓库，这里只需要仓库名字',
  oauth: {
    client_id: '创建 oauth 成功后的 client_id',
    client_secret: '创建 oauth 成功后的 client_secret',
  },
})
gitment.render('comments')
```

编辑后，重新编译并发布即可看到效果。

### tags
因为tags是单独一个页面展示，所以需要手动添加，输入以下命令就可以了

```bash
hexo new page tags
```

### 更新

```bash
cd themes/jane
git pull
```

### License

MIT
