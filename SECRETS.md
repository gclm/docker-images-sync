# 密钥设置说明

为了安全地同步镜像，需要在GitHub仓库中设置以下密钥：

## 必要的密钥

1. `ALIYUN_USERNAME` - 阿里云容器镜像服务的用户名
2. `ALIYUN_PASSWORD` - 阿里云容器镜像服务的密码
3. `DOCKER_USERNAME` - Docker Hub的用户名（可选，如果需要同步Docker Hub私有镜像）
4. `DOCKER_PASSWORD` - Docker Hub的密码（可选，如果需要同步Docker Hub私有镜像）
5. `GCR_USERNAME` - Google Container Registry的用户名（可选，如需同步GCR私有镜像）
6. `GCR_PASSWORD` - Google Container Registry的密码（可选，如需同步GCR私有镜像）

## 如何添加密钥

1. 在GitHub仓库页面，点击 `Settings` 标签
2. 在左侧菜单中找到 `Secrets and variables` -> `Actions`
3. 点击 `New repository secret` 按钮
4. 输入密钥名称（例如 `ALIYUN_USERNAME`）
5. 输入对应的值
6. 点击 `Add secret` 保存

## 注意事项

- 密钥添加后不可直接查看，只能更新或删除
- 确保密钥权限合适，最好使用有限权限的账户
- 定期更新密钥以提高安全性 