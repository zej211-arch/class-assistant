# 排课助手

培训机构智能排课工具。输入课程与教室信息，自动优化教室分配、避开冲突，生成可视化课表，支持多学期管理、导出 Excel 和打印 PDF。

纯前端单文件应用，无需后端、无需安装，打开 `index.html` 即可使用。

## 功能

- **课程录入**：课程名称、老师、星期、开始时间、上课时长（自动计算下课时间）、人数、偏好教室
- **教室配置**：教室名称、容量，默认全天可约
- **智能排课**：自动避开同教室同时段冲突、同老师同时段冲突、容量不足，优先分配偏好教室，排不下的课程标注具体冲突原因
- **可视化课表**：周视图 / 日视图，按老师、按教室筛选
- **多学期管理**：新建学期、保存排课、切换查看各学期课表、手动删除学期
- **导出与打印**：导出真正的 .xlsx 文件；一键打印 / 导出 PDF（A4 横向，适合贴墙）

## 本地使用

直接双击打开 `index.html` 即可，所有数据保存在浏览器本地（localStorage），不上传服务器。

## 部署到 GitHub Pages

### 方式一：网页上传（无需命令行）

1. 登录 GitHub，点右上角 **+ → New repository**
2. 仓库名填写（例如 `paike-assistant`），选择 **Public**，点 **Create repository**
3. 在仓库页点 **Add file → Upload files**
4. 把本文件夹里的 `index.html`、`.nojekyll`、`README.md` 拖进去（`.nojekyll` 是隐藏文件，如无法上传可忽略）
5. 点 **Commit changes**
6. 进入仓库 **Settings → Pages**
7. **Source** 选择 `Deploy from a branch`，Branch 选 `main`，目录选 `/ (root)`，点 **Save**
8. 等待 1–2 分钟，页面顶部会出现访问地址：`https://你的用户名.github.io/仓库名/`

### 方式二：命令行

```bash
git init
git add .
git commit -m "init 排课助手"
git branch -M main
git remote add origin https://github.com/你的用户名/paike-assistant.git
git push -u origin main
```

然后在仓库 Settings → Pages 中开启 GitHub Pages（同上第 6–8 步）。

## 说明

- 数据保存在浏览器本地，换浏览器或清除缓存后数据会丢失，建议定期用「导出 Excel」备份课表
- 打印课表时建议选择 A4 横向，效果最佳
