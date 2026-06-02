# 芽美口腔 - 暑期正畸活动 H5 落地页

## 📋 项目简介

这是一个为芽美口腔暑期正畸活动创建的H5响应式落地页，包含主活动页面和预约表单，采用深色高级感设计风格。

## 🎯 功能特性

- ✅ 深色主题 + 蓝色渐变高级感UI设计
- ✅ 响应式布局，适配移动端和桌面端
- ✅ 集成正畸科普视频播放
- ✅ 预约表单数据自动发送至飞书Webhook
- ✅ 专业的表单验证
- ✅ 流畅的动画交互效果

## 📁 项目结构

```
/Users/Admin/Desktop/暑期矫正活动/
├── index.html              # 主落地页
├── contact.html             # 预约表单页
├── orthodontics_video.mp4    # 正畸科普视频
├── vercel.json              # Vercel配置文件
└── README.md                # 部署指南
```

## 🚀 Vercel部署指南

### 方法一：通过Vercel网页部署（推荐）

**步骤1：准备文件**
1. 确保以下文件在同一文件夹中：
   - `index.html`
   - `contact.html`
   - `orthodontics_video.mp4`
   - `vercel.json`

**步骤2：访问Vercel**
1. 打开浏览器访问：https://vercel.com
2. 登录您的Vercel账户（支持GitHub、GitLab、Google账号）

**步骤3：创建项目**
1. 点击右上角的 **"Add New"** 按钮
2. 选择 **"Project"**
3. 向下滚动，找到 **"Import Third-Party Git Repository"** 部分
4. 点击 **"Or drop a folder here to deploy"** 或 **"Deploy Without Git"**
5. 将整个项目文件夹拖拽到上传区域

**步骤4：等待部署**
1. 系统会自动识别为静态网站
2. 等待几秒钟完成部署
3. 系统会生成一个 `.vercel.app` 域名的访问链接

**步骤5：完成！**
1. 访问生成的链接测试网站
2. 可以点击 **"Visit"** 查看网站
3. 如需绑定自定义域名，点击 **"Domains"** 进行配置

### 方法二：通过命令行部署

**前提条件：**
- 安装 Node.js (https://nodejs.org/)
- 安装 Vercel CLI：`npm install -g vercel`

**部署步骤：**
```bash
# 1. 进入项目目录
cd /path/to/暑期矫正活动

# 2. 登录Vercel
vercel login

# 3. 部署到预览环境
vercel

# 4. 部署到生产环境
vercel --prod
```

## ⚙️ 配置说明

### 飞书Webhook配置

预约表单已集成飞书Webhook通知功能。当客户提交预约时，数据会自动发送到您配置的飞书群。

**当前Webhook地址：**
```
https://open.feishu.cn/open-apis/bot/v2/hook/fa7c25e9-8caf-4c6c-a398-6360519361b3
```

**如需修改Webhook：**
1. 打开 `contact.html` 文件
2. 找到第505行：
   ```javascript
   const FEISHU_WEBHOOK_URL = 'YOUR_WEBHOOK_URL';
   ```
3. 将 `YOUR_WEBHOOK_URL` 替换为您的飞书Webhook地址

### 自定义域名

部署后可以绑定自定义域名：
1. 在Vercel项目设置中点击 **"Domains"**
2. 输入您的域名（如 `yamei.example.com`）
3. 按照提示配置DNS记录
4. 等待DNS生效（通常需要几分钟到24小时）

## 🎨 技术规格

- **设计风格**：深色高级感（参考Apple/Sony产品风格）
- **主色调**：蓝色渐变 (#00AEEF → #4DD0E1)
- **背景色**：深蓝黑 (#0A0E1A)
- **字体**：
  - 中文：Noto Sans SC
  - 英文：Inter
- **视频格式**：MP4 (H.264编码)
- **响应式断点**：
  - 桌面端：> 768px
  - 移动端：≤ 768px

## 🔧 本地测试

如需在本地测试：
```bash
# 使用Python内置服务器
cd /path/to/暑期矫正活动
python3 -m http.server 8000

# 然后在浏览器访问
http://localhost:8000
```

## 📞 技术支持

如有问题，请检查：
1. 所有文件是否在同一目录
2. 文件名是否完全匹配（包括大小写）
3. 视频文件是否完整可播放
4. 飞书Webhook是否有效

## 📄 许可证

本项目仅供芽美口腔活动使用。

---

**创建时间**：2026年6月2日  
**最后更新**：2026年6月2日
