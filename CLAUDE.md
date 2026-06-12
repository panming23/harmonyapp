# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

鸿蒙工具软件推广站点，纯静态 HTML 页面，托管在 GitHub Pages，通过自定义域名 `yingyong.panming.ccwu.cc` 提供服务。包含两个产品页面（网页文件传输、备注相机）和两个独立内容页（文件传输方式对比、工程拍照指南），共 5 个页面。

## 部署与推送


- **自定义域名:** `yingyong.panming.ccwu.cc`（由根目录 `CNAME` 文件配置）




## 技术栈

- 纯静态 HTML，无构建工具、无框架
- Bootstrap 3（`css/bootstrap.min.css` + `css/bootstrap-theme.min.css`）
- jQuery（`js/jquery.min.js`）+ Bootstrap JS（`js/bootstrap.min.js`）
- 无 package.json、无 npm、无 CI/CD

## 站点结构

```
index.html              # 首页，含站点介绍、价值说明、产品导航、延伸阅读
备注相机.html            # 备注相机产品页
网页文件传输.html         # 网页文件传输产品页
文件传输方式对比.html      # 独立内容页：7种文件传输方式对比分析
工程拍照指南.html         # 独立内容页：巡检拍照规范与技巧
robots.txt              # 爬虫规则
sitemap.xml             # 站点地图（5 个 URL，lastmod 需手动更新）
CNAME                   # GitHub Pages 自定义域名
BingSiteAuth.xml        # Bing 站长验证文件
42a0c42c-....txt        # 站点验证/统计用 UUID 文件
6cb2f115....txt         # 站点验证/统计用 UUID 文件
```

## SEO 配置规范

所有 5 个页面均配置了完整的 SEO 标签：Open Graph、Twitter Card、JSON-LD 结构化数据、meta robots，修改页面时需保持这些标签不变或同步更新。

更新 sitemap.xml 中 `<lastmod>` 日期时，同步更新所有三个 `<url>` 中的日期。

## 注意事项

- 文件名含中文，确保 git 和服务器 UTF-8 编码正确处理
- Vim swap 文件（`.html.css.swp`、`.index.html.swp`）被追踪在仓库中，修改时注意不要误操作这些文件
- 页面使用 `loading="lazy"` 对图片进行懒加载
- 图片资源体积较大（pic/ 目录下数 MB 级别），添加新图片时优先使用 WebP 格式压缩

