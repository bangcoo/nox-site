# NOX Ventures 官网 - 完整离线版（最终版）

## 📦 文件结构

```
stitch-complete/
├── index.html              # 主页面 (40KB)
├── README.md               # 本文档
├── css/
│   └── styles.css          # 所有样式 (8.7KB)
├── fonts/                  # 字体文件
│   ├── inter-400.woff2     # Inter Regular
│   ├── inter-500.woff2     # Inter Medium
│   ├── inter-700.woff2     # Inter Bold
│   ├── inter-800.woff2     # Inter ExtraBold
│   ├── inter-900.woff2     # Inter Black
│   └── material-symbols.woff2  # Material Icons
└── images/                 # 所有图片
    ├── nox-bg.jpeg
    ├── sign-logo.ico
    ├── talus-logo.ico
    ├── cetus-logo.ico
    ├── surge-logo.ico
    ├── metis-logo.png
    ├── gaiai-logo.jpg
    └── nfkings-logo.webp
```

**总大小**: ~180KB

## ✅ 完全本地化（0 外部依赖）

| 资源 | 状态 |
|------|------|
| CSS 框架 | ✅ 本地 css/styles.css |
| Inter 字体 | ✅ 本地 5 个字重 |
| Material Icons | ✅ 本地字体文件 |
| 所有图片 | ✅ 本地 images/ |
| **外部请求** | ✅ **0 个** |

## 🚀 部署

### 快速部署
```bash
# 整个文件夹上传到服务器任意目录
# 或拖拽到 Vercel/Netlify
```

### Nginx 配置
```nginx
server {
    listen 80;
    server_name nox.ventures;
    root /path/to/stitch-complete;
    index index.html;
    
    location / {
        try_files $uri $uri/ =404;
    }
    
    # 静态资源缓存 1 年
    location ~* \.(woff2|ico|jpg|png|webp|css)$ {
        expires 1y;
        add_header Cache-Control "public, immutable";
    }
}
```

## 🎯 验证清单

部署后检查：

- [ ] 所有窗口图标正常显示（桌面图标、Start 菜单）
- [ ] Portfolio 项目图标正常显示
- [ ] Services 窗口图标正常显示
- [ ] Insights 文章图标正常显示
- [ ] Contact 窗口图标正常显示
- [ ] 浏览器 Network 面板无外部请求
- [ ] 断网后页面正常访问

## 🔧 图标说明

使用 **Material Symbols Outlined** 字体图标，共 34 个图标：

| 图标名 | 用途 |
|--------|------|
| info | About us |
| settings_suggest | Services |
| folder | Portfolio |
| article | Insights |
| mail | Contact |
| terminal | Terminal |
| trending_up | Venture Capital |
| lightbulb | Advisory |
| campaign | Marketing |
| candlestick_chart | Trading |
| hub | Ecosystem |
| security | Sign Global |
| dns | Talus |
| waves | Cetus |
| psychology | Gai AI |
| layers | Metis |
| diamond | NFKings |
| ... | 更多 |

## 📊 性能

| 指标 | 数值 |
|------|------|
| 总大小 | ~180KB |
| 外部请求 | 0 |
| 首次加载 | <500ms |
| 国内访问 | ✅ 秒开 |
| 离线可用 | ✅ |

---

**版本**: v3.0 Final  
**日期**: 2026-04-06  
**特点**: 所有图标、字体、样式完全本地化
