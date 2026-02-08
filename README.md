# ACG 资源整理助手

一个智能的 ACG（动画、漫画、游戏）资源整理工具，帮助您从混乱的文本中快速提取和分类有用信息。

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Language](https://img.shields.io/badge/language-HTML%2FCSS%2FJS-orange.svg)
![Status](https://img.shields.io/badge/status-active-brightgreen.svg)

## ✨ 功能特性

### 🔍 智能文本解析
- **自动识别** - 从混乱的文本中提取车牌号、作者名、书名等信息
- **多种格式支持** - 支持自然语言、列表、混合文本等多种输入格式
- **智能分类** - 自动将提取的内容分为三类：
  - 🔢 ID/车牌 - 6-8位数字ID（支持Pixiv和18comic）
  - 🎮 作品/书籍 - 书名、作品名
  - 👤 作者/角色 - 作者名、画师名、角色名

### 🤖 AI 辅助识别
- **云端AI支持** - 通过 Cloudflare Worker 调用 AI 服务进行智能分析
- **深度理解** - 能够理解上下文，识别复杂的描述和指令
- **持续优化** - AI 模型持续学习，识别准确率不断提升

### 💾 本地数据管理
- **隐私保护** - 所有数据存储在浏览器本地，不上传任何服务器
- **导入导出** - 支持 JSON 格式的数据备份和恢复
- **历史记录** - 自动保存提取历史，支持按日期筛选查看

### 🎯 便捷操作
- **一键搜索** - 为每个条目生成直达链接：
  - Pixiv 作品/画师页面
  - 18comic 漫画页面
  - ExHentai 搜索
  - Google 搜索
- **批量打开** - 支持一键打开当前视图中的所有链接
- **双视图模式** - 分类视图和时间轴视图自由切换

## 🚀 使用方法

### 在线使用
直接访问：https://cheemsltt-boop.github.io/acg-helper/

### 本地使用
1. 克隆仓库
```bash
git clone https://github.com/cheemsltt-boop/acg-helper.git
```

2. 打开 `index.html` 文件即可使用

### 配置 AI 功能（可选）
如需使用 AI 智能识别功能，需要配置 Cloudflare Worker：

1. 创建 Cloudflare Worker
2. 在代码中修改 `WORKER_URL` 变量：
```javascript
const WORKER_URL = "https://your-worker.your-name.workers.dev";
```
3. Worker 代码需要实现代理到 AI 服务（如 DeepSeek）的功能

## 📖 使用示例

### 示例输入
```
这几天收集的好东西：
1. 历时122天打了9959个敌人
2. 这个画风感觉是Lvl3Toaster老师的#(呵呵)
3. [Racer] Onii-chan no Hanbun...
4. [禁漫漢化組](C106)[とかちのくに(結桐たかし)]kimassi(ラブライブ!)
5. 还有一个pixiv图 87110616 挺好看的
```

### 自动提取结果
- 🔢 **ID/车牌**: 87110616 → [直达 Pixiv](https://www.pixiv.net/artworks/87110616)
- 👤 **作者**: Lvl3Toaster → [搜索 Pixiv](https://www.pixiv.net/search/users?nick=Lvl3Toaster)
- 🎮 **作品**: Onii-chan no Hanbun → [搜索禁漫](https://18comic.vip/search/photos?search_query=Onii-chan%20no%20Hanbun)
- 👤 **作者**: 結桐たかし → [搜索 Pixiv](https://www.pixiv.net/search/users?nick=結桐たかし)

## 🛠️ 技术说明

### 技术栈
- **前端**: 纯 HTML5 + CSS3 + JavaScript (ES6+)
- **存储**: Browser LocalStorage
- **AI 代理**: Cloudflare Worker
- **设计**: 响应式布局，支持移动端

### 隐私说明
- ✅ 所有数据仅存储在浏览器本地
- ✅ 不收集任何用户个人信息
- ✅ AI 请求通过用户自建的 Worker 代理
- ✅ 无第三方追踪代码

### 浏览器兼容性
- Chrome / Edge / Firefox / Safari 最新版
- 支持移动端浏览器
- 需要启用 JavaScript 和 LocalStorage

## ⚠️ 免责声明

1. **内容来源**: 本工具仅提供文本解析和链接生成服务，不存储、不传播任何受版权保护的内容。

2. **用户责任**: 用户使用本工具提取的链接访问第三方网站时，需遵守当地法律法规和网站使用条款。

3. **版权尊重**: 请尊重原作者版权，支持正版。本工具生成的链接仅供个人学习研究使用。

4. **年龄限制**: 本工具可能生成指向成人内容的链接，使用者必须年满18岁（或当地法定成年年龄）。

5. **免责声明**: 开发者不对用户使用本工具产生的任何后果负责，包括但不限于版权纠纷、法律问题等。

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📄 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

---

**注意**: 本项目仅供学习交流使用，请合理使用，遵守相关法律法规。
