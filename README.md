# Hexo
> Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 Markdown（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

## 安装前提

- [官方文档](https://hexo.io/zh-cn/docs/)
- nodejs&npm(yarn)
- git

```sh
# 安装 hexo-cli
npm install hexo-cli -g
npm install -g yarn
# 拉取远程仓库
git clone -b hexo git@github.com:DukeBode/DukeBode.github.io.git
# 安装依赖
yarn install
# 更新依赖

# 更新部署
hexo deploy
```
## 复制主题配置
```
cp node_modules/hexo-theme-landscape/_config.yml _config.landscape.yml
```
