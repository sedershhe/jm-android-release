# Security Policy

## Never Commit

- 账号、密码、Cookie、访问令牌
- Android Keystore、签名密码和 `keystore.properties`
- GitHub Codespaces Secrets 或 Actions Secrets
- 包含用户下载记录、搜索记录或登录状态的日志

## Credential Handling

`jm3.4.7` 的 `option.yml` 使用专用测试账号。该配置仍不得提交到仓库，安卓应用必须
提供账号修改窗口；测试构建通过 Codespaces Secrets 注入，正式 APK 不内置账号密码。
用户会话应保存在 Android Keystore 保护的存储中。构建签名只允许通过受保护的
GitHub Actions 环境读取 Secrets。

## Reporting

发现密钥泄漏时先阻止继续提交，再撤销并轮换密钥。不要在公开 Issue 中粘贴密钥。
