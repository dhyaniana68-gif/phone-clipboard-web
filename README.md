# Phone Clipboard Web

这是“手机输入 → 电脑剪贴板同步”项目的 **GitHub Pages 静态网页部署仓库**。它只承载手机端 H5，不是完整产品源码仓库。

## 仓库职责

```text
phone-clipboard-web/
├── index.html   # 当前手机端静态 H5（HTML / CSS / JavaScript）
├── fonts/       # 页面引用的本地字体资源
├── .nojekyll    # GitHub Pages 静态部署标记
└── README.md    # 本说明
```

完整桌面端、测试和产品设计资料维护在私有综合仓库：

```text
creative-projects-and-tools-hub/
└── 01-apps-独立软件工具/
    └── phone-to-pc-clipboard/
```

## 部署地址

```text
https://dhyaniana68-gif.github.io/phone-clipboard-web/
```

## 数据边界

本仓库不应保存：

- Windows 桌面端源码和本机配置；
- 运行日志；
- room / key；
- 完整配对 URL 或二维码；
- token、密码和其他认证信息。

配对信息由运行时 URL Fragment 提供，不应写死在公开仓库文件中。

## 当前安全行为

`index.html` 仅允许通过 Web Crypto / AES-GCM 加密发送。URL 配对信息缺失、配置无效、Web Crypto 不可用或密钥导入失败时，页面会显示“配对失败”并保持输入和发送控件禁用，不会降级为明文传输。

完整安全设计、ACK 语义和修复优先级以私有主项目 README 为准。

## 发布与维护约定

1. `index.html` 保持为可直接部署的静态入口。
2. `fonts/` 与页面引用路径同步维护，不单独移动字体文件。
3. 修改正式 H5 时，应同时核对私有主项目中的 `web/index.html` 与本仓库版本，避免两个副本出现逻辑漂移。
4. 公开仓库只保存部署所需文件；产品设计、桌面端代码、测试和运行说明继续在私有主项目维护。
5. 发布前至少检查：页面可加载、配对解析正常、加密路径可用、发送状态与 ACK 展示正常、无敏感数据写入源码。
