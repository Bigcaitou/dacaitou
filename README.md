[TOC]
# 首页
## 内容

本站点  由 @Bigcaitou 维护，内容包括但不限于如下：
* 个人主站
* 技术分享


## 站点搭建

本站点的搭建通过如下工具实现：

* 静态网站文档生成器： [docsify](https://docsify.js.org/#/)
* 代码高亮： [prismjs](https://prismjs.com/)
* 代码及文档托管： [github](https://www.github.com/Bigcaitou/dacaitou)
    
    ```yml
    pages:
        stage: deploy
        script:
        - mkdir .public
        - cp -r docs/* .public
        - mv .public public
        artifacts:
            paths:
            - public
        only:
        - master
    ```

## 协作指引

本项目文件树如下：

```bash
└── docs
    ├── README.md # 本站点说明
    ├── dir_demo
    │   ├── README.md #
    │   ├── doc_demo1.md # 业务文档
    │   ├── images # 文档内图片，只对TAF目录下生效
    │   │   ├── image-demo1.png
    │   │   ├── image-demo2.png
    │   └── doc_demo2.md
    ├── _navbar.md # 导航栏
    ├── _sidebar.md # 侧边栏
    ├── docsify@4.12.1 # 当前版本
    │   ├── lib # 依赖库
    │   │   ├── docsify.min.js # docsify核心js
    │   │   └── plugins
    │   │       └── search.js ## 插件
    │   └── themes
    │       └── vue.css ## 样式库
    └── index.html # docsify核心入口文件
```

 
 

