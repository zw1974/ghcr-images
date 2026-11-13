# ghcr-images

公开仓库，用 GitHub Actions 构建容器镜像并推送到 GHCR。包名为 `ghcr.io/zw1974/ghcr-images`，用 tag 区分子镜像，可匿名拉取，不依赖 Docker Hub。

## 镜像列表

| 拉取命令 | Dockerfile |
| --- | --- |
| `docker pull ghcr.io/zw1974/ghcr-images:dtk-api` | docker/Dockerfile |
| `docker pull ghcr.io/zw1974/ghcr-images:dtk-downloader` | docker/Dockerfile.downloader |
| `docker pull ghcr.io/zw1974/ghcr-images:dtk-transcriber` | docker/Dockerfile.transcriber |

源码来自上游 Evil0ctal/Douyin_TikTok_Download_API，构建全部在 GitHub 侧完成，本地无需访问 github.com 或 hub.docker.com。

## 说明

- 包名必须与本仓库名一致，否则 `GITHUB_TOKEN` 推送会被拒（`permission_denied`）。
- browser-rpc 镜像故意不发布：它要从固定的第三方 commit 安装 CloakBrowser，保持本地构建。
- 当前只构建 linux/amd64；如需 arm64，在 workflow 的 `platforms` 加上 `linux/arm64`，并加入 `docker/setup-qemu-action`。
