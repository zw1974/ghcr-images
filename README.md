# ghcr-images

公开仓库，用于在 GitHub Actions 上构建容器镜像并推送到 GHCR，镜像可匿名拉取，无需登录、不依赖 Docker Hub。

## 产出镜像

| 镜像 | Dockerfile |
| --- | --- |
| ghcr.io/zw1974/dtk-api | docker/Dockerfile |
| ghcr.io/zw1974/dtk-browser | docker/Dockerfile.browser |
| ghcr.io/zw1974/dtk-downloader | docker/Dockerfile.downloader |
| ghcr.io/zw1974/dtk-transcriber | docker/Dockerfile.transcriber |

源码来自上游 
Evil0ctal/Douyin_TikTok_Download_API，构建全程在 GitHub 侧完成。

## 本地使用

```
docker pull ghcr.io/zw1974/dtk-api:latest
```

无需 docker login：包继承本公开仓库的可见性。
