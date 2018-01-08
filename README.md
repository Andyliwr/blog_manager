# 月光倾城的代码小屋
## 更新历史
1. 2017年12月29日 开始写更新记录

## 介绍
使用hexo来管理以及发布网站博客，只需要通过写markdown文件就可以发布博客。

## 使用
1. 克隆本项目并安装
```
git clone https://github.com/AndyliStudio/BehavioralGeneticsSQL-blog.git
cd BehavioralGeneticsSQL-blog
npm install
npm install hexo-cli -g
hexo server
```

2. 新建终端，开始写博客
```
hexo new post "title" //新建博客文章
hexo new page "title" //新建页面
hexo new draft "title" //新建草稿
```

3. 发布博客
```
hexo clean
hexo generate
hexo deploy
```

## 常见问题
1. `hexo server`启动hexo后发现打开`http://localhost:4000`出现404错误

关闭hexo，在终端中输入`netstat -tunpl`看看4000端口是否被占用了，如果已被占用，你可以通过`hexo server -p 5000`在另一个端口启动hexo。如果不是端口占用引起的访问页面错误，你可以试试打开`127.0.0.1:4000`.

2. 动态标题 

```
<%
  var title = '';
  var subtitle = '';
  if(page.title === "音乐列表"){
    title = '音乐'
    subtitle = '一杯敬明天，一杯敬过往'
  }else if(page.title === "记事列表"){
    title = '记事'
    subtitle = '等自己老了，搬凳子做在自家屋檐下，这些成了最宝贵的回忆'
  }else if(page.title === "涂鸦列表"){
    title = '涂鸦列表'
    subtitle = '爱上一个人，也会爱上她喜欢的'
  }
%>
```
3. 使用font-awaresome需要自己定义类
```
.fa-times-circle
  font-style: normal
  font-family: 'FontAwesome'
  &:before
    content: "\f057"
```
