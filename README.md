# 中职财经商贸课程平台 - 示例仓库


此仓库为示范性的中职财经商贸课程网站（静态前端），包含课程首页、资源、讨论区与作业列表等模块。


## 仓库结构
```
vocational-course-site/
├─ index.html
├─ assets/
│ ├─ css/styles.css
│ ├─ js/app.js
│ └─ img/logo.png
├─ materials/
│ ├─ syllabus.pdf
│ ├─ lesson1.pdf
│ └─ exercises.xlsx
└─ README.md
```


## 功能说明（示范）
- 课程目录、资源下载（通过 `materials/` 目录托管文件）
- 作业与测验列表（前端示范）
- 讨论区（前端存储示范）
- 登录示范（目前为前端模拟，建议接入学校 SSO / 后端认证）


## 自定义与对接建议
1. 后端：建议接入 REST API 或 GraphQL，用于用户认证（SSO）、课程数据、作业提交、成绩管理与讨论区持久化。
2. 文件托管：可使用 GitHub 仓库的 `materials/` 临时托管（公开仓库），或接入学校 OSS（如阿里云 OSS、七牛）以满足大文件与权限控制需求。
3. 教学工具对接：对接 Zoom/腾讯会议/钉钉直播时，教师端界面需要实现直播调度和签到功能。
4. 数据库：用户、课程、成绩建议使用关系型数据库（MySQL/Postgres），讨论与日志可以考虑 Elasticsearch 或 Redis 做缓存。


## 部署说明（GitHub Pages）
1. 在 GitHub 创建一个新仓库（例如 `vocational-course-site`）。
2. 将本地文件按上述结构推送到仓库。
3. 进入仓库设置 -> Pages，选择 `main` 分支及 `/ (root)` 目录作为发布源。
4. 几分钟后，站点将在 `https://<your-username>.github.io/<repo-name>/` 可访问。


## 部署到其他平台
- Netlify / Vercel：连接 Git 仓库，选择构建 & 发布目录为根目录（无需额外构建，静态站点直接部署）。
- 学校服务器：通过 FTP/SCP 上传到 Web 根目录，或将静态资源放在 CDN 后端进行分发。


## 未来扩展建议
- 增加教师端与学生端的独立仪表盘。
- 集成题库系统、自动评测（选择题、判断题）与作业批改流水线。
- 支持 LTI（Learning Tools Interoperability）与教务系统互联。






---


*说明*：此仓库为教学示范，需结合学校信息化要求做权限与隐私保护（如学生信息不得公开）。
