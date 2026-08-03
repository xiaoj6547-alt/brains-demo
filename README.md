# 工银BRAINS智能分流演示系统

该目录用于发布GitHub Pages公开演示入口。`index.html` 是自包含单文件，内含页面、
样式、图标、脚本和脱敏离线回放数据，不依赖本地服务或外部CDN。

重新生成：

```bash
cd ../aliyun
node scripts/sync-assets.mjs
node scripts/build-portable-html.mjs ../github-pages/index.html
```

配置 `BRAINS_PUBLIC_API_BASE` 后重新生成，可让公开网页跨域调用阿里云函数计算
的 `/api/*` 接口；接口不可用时仍自动回退到内置演示数据。
