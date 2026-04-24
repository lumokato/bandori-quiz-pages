# Bandori Quiz Pages

测测你与哪个 Bangdream 角色最接近 —— Cloudflare Pages 前端项目。

## 项目结构

```
bandori-quiz-pages/
├── index.html       # 前端页面（题库 + 算分 + 结果展示）
├── wrangler.toml    # Cloudflare Pages 配置
├── images/          # 角色图片（联合开发者补充）
└── README.md
```

## 部署方式

### 方式 A：GitHub 连接（推荐）

1. 在 Cloudflare Pages 选择 `Connect to Git`
2. 选择本仓库 `lumokato/bandori-quiz-pages`
3. 构建配置：
   - Build command：留空
   - Build output directory：`.`

### 方式 B：Wrangler 手动部署

```bash
npx wrangler login
npx wrangler pages deploy . --project-name=bandori-test
```

## 后端 API

测试结果通过前端异步提交到独立后端：

```
https://bandori-api.120224.xyz
```

后端仓库：[lumokato/bandori-quiz-api](https://github.com/lumokato/bandori-quiz-api)

## 自定义域名

- 生产环境：`quiz.fueee.moe`
- Cloudflare 默认：`bandori-test.pages.dev`（自动重定向到生产域名）

## 协作开发

1. Fork 本仓库
2. 角色图片放入 `images/` 目录
3. 提交 Pull Request
