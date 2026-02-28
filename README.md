# OUDKT 欧德凯特智能导航中心 🚀

> 一个现代化的个人主页/服务导航系统，灵感来自 Homepage 和 Home-Vue

## 这是啥？🤔

这是欧德凯特（OUDKT）的智能导航中心。一个集服务监控、快捷书签、搜索导航于一体的现代化主页。

**特色功能：**
- 🎨 现代化设计（参考 gethomepage/homepage）
- 📊 服务卡片展示（CPU、内存监控）
- 🔖 快捷书签管理
- 🔍 智能搜索（支持直接输入 URL 跳转）
- ⚙️ 完整的后台管理系统
- 📱 响应式布局（手机也能用）
- 💾 本地存储（数据保存在浏览器）

## 怎么用？🛠️

### 看主页
直接打开 `index.html` 就行了。

或者访问：https://cshaizhihao.github.io/oudkt-homepage/

### 管理内容
1. 点右上角的"管理"按钮，或者点右下角的浮动按钮
2. 输入账号：`admin`
3. 输入密码：`admin`
4. 然后就可以管理服务和书签了！

**可以管理：**
- ✅ 服务卡片（名称、图标、描述、CPU、内存）
- ✅ 快捷书签（名称、图标、URL、分类）

## 文件说明📁

```
oudkt-homepage/
├── index.html      # 主页（服务导航中心）
├── admin.html      # 管理后台（管理服务和书签）
└── README.md       # 你现在看的这个文件
```

## 技术栈🔧

- HTML5 + CSS3 + JavaScript（原生，不依赖框架）
- Font Awesome 6.4（图标库）
- Inter 字体（Google Fonts）
- LocalStorage（数据存储）

## 特色功能✨

### 1. 服务卡片
显示你的各种服务，支持：
- 自定义图标（Font Awesome）
- 服务描述
- CPU 和内存使用率显示
- 在线状态指示

### 2. 快捷书签
快速访问常用网站：
- 支持自定义图标
- 分类管理
- 一键跳转

### 3. 智能搜索
搜索栏支持：
- 搜索服务和书签
- 直接输入 URL 跳转（http:// 或 https://）

### 4. 管理后台
完整的后台管理系统：
- 添加/编辑/删除服务
- 添加/编辑/删除书签
- 实时预览

## 常见问题❓

**Q: 数据存在哪里？**  
A: 存在浏览器的 LocalStorage 里，换个浏览器就没了。

**Q: 怎么改密码？**  
A: 打开 `admin.html`，搜索 `username === 'admin' && password === 'admin'`，改成你想要的。

**Q: 图标怎么选？**  
A: 去 [Font Awesome](https://fontawesome.com/icons) 找图标，复制类名（比如 `fa-github`）。

**Q: 能部署到 VPS 吗？**  
A: 能！直接把文件扔到 Nginx/Apache 的 web 目录就行。

**Q: 为什么没有后端？**  
A: 因为这是纯前端项目，数据存在浏览器里。如果需要多设备同步，可以自己加个后端。

## 部署到 VPS🌐

### 方法 1：Nginx
```bash
# 复制文件到 web 目录
cp -r oudkt-homepage /var/www/html/

# 配置 Nginx
server {
    listen 80;
    server_name your-domain.com;
    root /var/www/html/oudkt-homepage;
    index index.html;
}
```

### 方法 2：Docker
```bash
# 创建 Dockerfile
FROM nginx:alpine
COPY . /usr/share/nginx/html

# 构建并运行
docker build -t oudkt-homepage .
docker run -d -p 80:80 oudkt-homepage
```

### 方法 3：GitHub Pages
1. 把代码推到 GitHub 仓库
2. 去仓库设置 → Pages
3. Source 选 `master` 分支
4. 等几分钟就好了

## 设计灵感🎨

- **gethomepage/homepage** - 服务卡片布局和功能设计
- **JLinMr/Home-Vue** - 简洁的导航理念
- **现代 Dashboard 设计** - 配色和交互

## 作者👨‍💻

- 设计：Koma（AI 助理）
- 开发：Koma
- 老板：Zaki

## 许可证📄

随便用，不用问我。

---

**提示：** 这个项目适合作为个人主页、服务导航、团队内部工具使用。数据存在本地，安全可靠！🔒
