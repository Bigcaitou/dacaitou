[TOC]
## todos
* [ ] 域名
* [ ] gittalk
    * 官方文档 https://github.com/gitalk/gitalk
    * env
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
        clientID: '${{ env.GITTALK_CLIENTID }}',
        clientSecret: '${{ env.GITTALK_CLIENTSECRET }}',
        repo: 'dacaitou',
        owner: 'Bigcaitou',
        admin: ['Bigcaitou'],
        title: location.hash.match(/#(.*?)([?]|$)/)[1],
        id: location.hash.match(/#(.*?)([?]|$)/)[1],      // Ensure uniqueness and length less than 50
        })
        // gitalk.render('gitalk-container')
    </script>
    ```
* [ ] wordpress
    * 官方文档：https://ubuntu.com/tutorials/install-and-configure-wordpress#6-configure-wordpress-to-connect-to-the-database
    * apache
    * mysql
    * wp recover
    * wp config
    * host nginx
    * theme → md
* 图床
    * https://sspai.com/post/61624
* cdn加速
