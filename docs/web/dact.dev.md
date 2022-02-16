[TOC]
## dact.dev实现细节
## docsify

## github pages
### 自定义域名

## gittalk

[gitalk](https://github.com/gitalk/gitalk)
   
    * github page action
        * https://github.com/marketplace/actions/github-pages
    
cat `index.html`

```js
<!-- gittalk组件 -->
<link rel="stylesheet" href="//unpkg.com/gitalk/dist/gitalk.css">
<script src="//unpkg.com/gitalk/dist/gitalk.min.js"></script>
<script src="//unpkg.com/docsify/lib/plugins/gitalk.min.js"></script>

<script>
    var gitalk = new Gitalk({
    clientID: 'GITTALK_CLIENTID',
    clientSecret: 'env.GITTALK_CLIENTSECRET',
    repo: 'dacaitou',
    owner: 'Bigcaitou',
    admin: ['Bigcaitou'],
    title: location.hash.match(/#(.*?)([?]|$)/)[1],
    id: location.hash.match(/#(.*?)([?]|$)/)[1],      // Ensure uniqueness and length less than 50
    })
    // gitalk.render('gitalk-container')
</script>
```
### clientID和clientSecret在公网中暴露的问题

之前担心clientID和clientSecret在公网中暴露会有安全问题，但是发现了官方issue里已经有人解答了：[Bug？暴露 Client_id和Client_secret ？ #150](https://github.com/gitalk/gitalk/issues/150)

> @booxood:
> * 获取或修改 GitHub 用户数据，需要 token，为了拿到 token，除了需要 OAuth App 的 client_id 和 client_secret 外，还需要一个 Authorization Code。
> * 这个 code 是 GitHub 登录授权完成时，在跳转回 redirect_uri 的查询参数拿到的， redirect_uri 必须是在 OAuth App 配置的 callback URL 域名下。
> * 这样即使别人用了你的 client_id 和 client_secret ，跳转之后也拿不到 code，所以，有 client_id 和 client_secret 也做不了什么。

## wordpress 数据迁移

* 官方文档：https://ubuntu.com/tutorials/install-and-configure-wordpress#6-configure-wordpress-to-connect-to-the-database
* apache
* mysql
* wp recover
* wp config
* host nginx
* theme → md

## 图床
//TODO
* https://sspai.com/post/61624

## cdn加速
//TODO