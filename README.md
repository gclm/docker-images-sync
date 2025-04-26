# Docker镜像同步工具

通过GitHub Issues实现Docker镜像到阿里云容器镜像服务的自动同步。本工具基于[image-syncer](https://github.com/AliyunContainerService/image-syncer)开发，使用GitHub Actions自动化流程。

## 使用方法

1. 创建一个新的Issue，使用提供的"镜像同步请求"模板
2. 填写Issue标题，确保包含`image-sync`关键词
3. 在Issue正文中按照以下格式列出需要同步的镜像：
   ```
   源镜像地址: 目标镜像地址
   ```
4. 提交Issue后，GitHub Actions将自动触发同步流程
5. 同步完成后，机器人会在Issue中添加评论，显示同步结果

## 示例

```
docker.io/library/nginx:latest: registry.cn-hangzhou.aliyuncs.com/sealos/nginx:latest
k8s.gcr.io/kube-apiserver:v1.24.0: registry.cn-hangzhou.aliyuncs.com/sealos/kube-apiserver:v1.24.0
```

## 功能特点

- 自动解析Issue中的镜像配置信息
- 支持多种镜像源（Docker Hub、GCR等）
- 提供详细的同步结果报告
- 使用模板减少配置错误

## 注意事项

- 请确保遵循正确的格式填写镜像信息
- 如需同步私有仓库镜像，请联系管理员配置相应的仓库认证信息
- 详细的密钥配置说明请参考[SECRETS.md](./SECRETS.md) 