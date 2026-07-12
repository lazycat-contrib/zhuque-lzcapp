# ZhuQue - LazyCat 应用包

每天定时检查 ZhuQue 镜像，并支持 `v*` tag 和手动触发懒猫官方商店与喵喵私有商店发布。

朱雀（ZhuQue）是一个现代化 Web 应用，支持 JWT 认证和 Webhook 功能。

## 配置要求

在部署时需要配置以下参数：

| 参数 | 类型 | 说明 | 默认值 |
|------|------|------|--------|
| `webhook_token` | secret | Webhook 令牌，用于 webhook 验证 | 必填 |
| `rust_log` | string | 日志级别：error, warn, info, debug, trace | info |
| `timezone` | string | 时区设置，如 Asia/Shanghai | Asia/Shanghai |

**注意**：JWT_SECRET 自动生成稳定密钥，无需手动配置。

## 功能特点

- JWT 认证机制
- Webhook 支持
- 数据持久化存储
- 时区配置（Asia/Shanghai）

## 开发

```bash
# 安装 lzc-cli
npm install -g @lazycatcloud/lzc-cli

# 部署开发环境
lzc-cli project deploy

# 查看日志
lzc-cli project log -f
```

## 构建

```bash
# 构建发布包
lzc-cli project release -o zhuque.lpk
```

## 来源

- 镜像: ghcr.io/mtvpls/zhuque:latest
- 原项目: https://github.com/mtvpls/zhuque# zhuque-lzcapp
