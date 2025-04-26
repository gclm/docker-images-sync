# 贡献指南

感谢您对Docker镜像同步工具的兴趣！以下是参与贡献的一些指南。

## 报告问题

如果您发现了bug或有新功能建议，请通过GitHub Issues报告：

1. 使用清晰的标题描述问题
2. 提供详细的复现步骤
3. 如果可能，附上错误信息和截图

## 提交代码

1. Fork本仓库
2. 创建您的特性分支：`git checkout -b feature/your-feature-name`
3. 提交您的更改：`git commit -m '添加某某功能'`
4. 推送到您的分支：`git push origin feature/your-feature-name`
5. 提交Pull Request

## 代码规范

- 保持代码风格一致
- 添加必要的注释
- 确保GitHub Actions工作流能够正常运行
- 更新相关文档

## 镜像源配置

如果您需要添加对新的镜像源的支持：

1. 修改`auth.yaml`文件，添加新的镜像源认证配置
2. 更新README.md文档
3. 确保新增的镜像源在GitHub Actions中有对应的密钥配置

## 测试

在提交Pull Request前，请确保：

1. 本地测试通过
2. GitHub Actions工作流能够正常运行
3. 所有功能按预期工作 