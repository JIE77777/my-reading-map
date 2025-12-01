🌍 My Reading Map (部署与使用指南)

这是你的专属阅读世界地图，包含安全认证功能。

🔐 认证信息

为了保护你的阅读隐私，项目已开启访问认证。

默认认证码: BytheLakeS

状态保持: 输入一次后，系统会记住你的登录状态，无需重复输入（除非手动点击右侧栏的“锁定”按钮）。

📁 快速部署指南

由于本项目采用单文件架构 (Single File Architecture)，部署非常简单，无需复杂的构建工具（如 Webpack/Vite）或后端服务器。

方案 A：GitHub Pages (最推荐，永久免费)

创建仓库：在 GitHub 上新建一个仓库（例如命名为 my-reading-map）。

上传文件：将 reading_map.html 文件重命名为 index.html，然后上传到该仓库的根目录。

开启 Pages：

进入仓库的 Settings (设置) -> Pages (页面)。

在 Branch (分支) 选项下，选择 main (或 master) 分支，文件夹选择 / (root)。

点击 Save。

访问：等待 1-2 分钟，GitHub 会生成一个链接（如 https://yourname.github.io/my-reading-map/），访问即可使用。

方案 B：Netlify Drop (最快，无需注册)

访问 Netlify Drop。

将包含 reading_map.html 的文件夹直接拖入网页中的虚线框区域。

等待几秒钟，Netlify 会给你一个随机生成的网址（如 https://flamboyant-darwin-12345.netlify.app）。

方案 C：本地运行

直接双击 reading_map.html 文件，使用 Chrome、Edge 或 Safari 浏览器打开即可完全正常使用。

数据存储在浏览器的 LocalStorage 中，只要不清除缓存，数据就会一直保留在你的这台电脑上。

⚙️ 项目结构优化说明

虽然为了部署便捷性保持了单文件结构，但在代码内部我们进行了清晰的模块划分：

Auth Module: 负责遮罩层的显示、隐藏及 Token 管理。

State Module: 负责 books 数据的加载、保存和导入导出。

Map Module: 负责 Leaflet 地图初始化、图层管理和聚合逻辑。

UI Module: 负责 Modal 弹窗、FAB 按钮和工具栏交互。

Service Module: 负责 Geocoding (OpenStreetMap API) 和 html2canvas 截图服务。

🛠️ 数据备份

重要：建议定期点击右侧工具栏的 “下载图标” 导出 .json 数据备份。

如果你更换设备或清除浏览器缓存，可以通过 “上传图标” 恢复数据。
