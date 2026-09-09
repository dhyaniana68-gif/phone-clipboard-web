# Phone Clipboard Web

这是“手机输入 → 电脑剪贴板同步”项目的 **GitHub Pages 静态网页部署仓库**。

本仓库只负责托管手机端 H5 页面，不保存 Windows 桌面端源码、运行配置、日志、配对凭据、room/key 或其他私密数据。

## 仓库职责

```text
phone-clipboard-web/
├── index.html   # 手机端静态 H5 页面（HTML / CSS / JavaScript）
├── fonts/       # 页面使用的本地字体资源
├── .nojekyll    # GitHub Pages 静态部署标记
└── README.md    # 本说明
```

完整桌面端与产品源码位于私有综合仓库：

`creative-projects-and-tools-hub/01-apps-独立软件工具/phone-to-pc-clipboard/`

## 部署地址

GitHub Pages：`https://dhyaniana68-gif.github.io/phone-clipboard-web/`

## 维护约定

- `index.html` 保持为可直接部署的静态入口；除非同步修改引用，不随意移动 `fonts/`。
- 不向本仓库提交桌面端配置、日志、密钥、完整配对链接或其他敏感信息。
- 产品设计文档、桌面端代码和运行说明统一维护在私有综合仓库，本仓库只保留公开部署所需文件。
