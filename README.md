# 发电机租赁 热更新服务器

##  构建成功!

### 构建信息
- **应用名称**: 发电机租赁
- **版本号**: 1.0.10
- **版本码**: 1010
- **文件大小**: 0.41 MB
- **构建工具**: HBuilderX 4.87
- **Vue 版本**: 3
- **源文件**: F:\未交付\generator-leasing-master\unpackage\dist\build\app-plus\__UNI__147ADA1.wgt

##  快速部署

### 1. 上传文件
将 `deploy/` 目录下的所有文件上传到 GitHub 仓库:
- `index.html` - 状态页面
- `update.json` - 更新配置文件
- `update.wgt` - 热更新资源包 (0.41 MB)
- `update-1.0.10.wgt` - 版本备份
- `README.md` - 说明文档
- `.nojekyll` - GitHub Pages 配置文件

### 2. 启用 GitHub Pages
1. 访问仓库: https://github.com/000zZz000/generator-app-updates
2. Settings → Pages
3. Source: Deploy from a branch
4. Branch: main
5. Folder: / (root)
6. Save

### 3. 访问地址
- 状态页面: https://000zZz000.github.io/generator-app-updates/
- 配置文件: https://000zZz000.github.io/generator-app-updates/update.json
- 资源包: https://000zZz000.github.io/generator-app-updates/update.wgt

##  App 配置

在 App 项目的 `static/update-config.json` 中添加:

```json
{
  "configUrl": "https://000zZz000.github.io/generator-app-updates/update.json",
  "checkInterval": 86400,
  "autoDownload": true
}
```

##  更新内容

版本 1.0.10 更新内容:

1. 修复动态导入警告
2. 添加热更新功能
3. 优化应用性能

## ⚠️ 构建警告（可忽略）

构建时出现以下警告，不影响功能:

```
1. api.js is dynamically imported but also statically imported
2. userRole.js is dynamically imported but also statically imported
```

这些警告是因为在 `auth.js` 中使用了动态导入，但在其他文件中又使用了静态导入。
这只是 Vite 的优化警告，不影响应用功能。

##  更新流程

### 开发者:
1. 修改代码并测试
2. 在 HBuilderX 中重新构建: 发行 → 原生App-本地打包 → 生成本地打包App资源
3. 运行部署脚本: `npm run deploy:github`
4. 上传新文件到 GitHub

### 用户:
1. App 启动时自动检查更新
2. 检测到新版本后提示用户
3. 下载并安装 wgt 包
4. 重启应用加载新版本

##  故障排除

### 1. 无法下载更新
- 检查网络连接
- 确认 GitHub Pages 已启用
- 检查 URL 是否正确

### 2. 安装失败
- 确保 wgt 文件完整
- 检查设备存储空间
- 确认 App 版本兼容

### 3. 页面无法访问
- 等待 1-2 分钟缓存更新
- 检查仓库是否为 Public
- 确认文件已上传成功

##  版本历史

### 1.0.10 (2026-01-13)
版本 1.0.10 更新内容:

1. 修复动态导入警告
2. 添加热更新功能
3. 优化应用性能

---
*此文件由部署脚本自动生成*
*最后更新时间: 2026/1/13 17:04:36*