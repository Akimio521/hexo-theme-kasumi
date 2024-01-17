# hexo-theme-kasumi
**霞（かすみ）** 一款基于[hexo-theme-butterfly](https://github.com/jerryc127/hexo-theme-butterfly)修改的主题

## 安裝
### Git 安裝
# 稳定版本
```shell
git clone -b main https://github.com/Akimio521/hexo-theme-kasumi.git themes/kasumi
cp -rf ./themes/kasumi/_config.yml ./_config.kasumi.yml
```

## 应用主题
修改hexo的配置文件`_config.yml`，把主題改为`kasumi`
```yml
theme: Kasumi
```

## 推荐插件安装
**若不按照可能会造成部分样式显示错误**
- 优先度0：若不安装主题无法启用
- 优先度1：主题部分功能无法使用，需要修改`.config.yml`部分默认设置
- 有限度2：仅仅是推荐安装
### 优先度0
```shell
npm install hexo-renderer-pug hexo-renderer-stylus --save # pug以及stylus的渲染器
```

### 优先度1
```shell
npm i --save hexo-wordcount # 字数统计
npm install hexo-butterfly-tag-plugins-plus --save # 外挂标签
npm uninstall hexo-renderer-marked --save && npm install hexo-renderer-kramed --save # 更换markdown渲染方式：hexo-renderer-kramed
```

### 优先度2
```shell
npm install hexo-abbrlink2 --save # 短链安装
npm install hexo-algoliasearch --save # algolia搜索
```

## config配置
```
# hexo-abbrlink2：
## 修改
permalink: posts/:abbrlink/
## 增加
abbrlink:
  start: 1000 # the first id, default 0
# algoliasearch：
## 增加
algolia:
  appId: "Z7A3XW4R2I"
  apiKey: "12db1ad54372045549ef465881c17e743"
  adminApiKey: "40321c7c207e7f73b63a19aa24c4761b"
  chunkSize: 5000
  indexName: "my-hexo-blog"
  fields:
    - content:strip:truncate,0,500
    - excerpt:strip
    - gallery
    - permalink
    - photos
    - slug
    - tags
    - title
```

# Star History
<a href="https://github.com/Akimio521/hexo-theme-Kasumi/stargazers">
    <img width="500" alt="Star History Chart" src="https://api.star-history.com/svg?repos=Akimio521/hexo-theme-kasumi&type=Date">
</a>