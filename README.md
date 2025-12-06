<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PixelNav Station V28.0 说明文档</title>
    <style>
        body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif; line-height: 1.6; color: #333; max-width: 800px; margin: 0 auto; padding: 20px; }
        h1 { border-bottom: 1px solid #eaecef; padding-bottom: 0.3em; }
        h2 { border-bottom: 1px solid #eaecef; padding-bottom: 0.3em; margin-top: 24px; }
        code { background-color: #f6f8fa; padding: 0.2em 0.4em; border-radius: 3px; font-family: SFMono-Regular, Consolas, "Liberation Mono", Menlo, monospace; font-size: 85%; }
        pre { background-color: #f6f8fa; padding: 16px; overflow: auto; border-radius: 3px; }
        blockquote { margin: 0; padding: 0 1em; color: #6a737d; border-left: 0.25em solid #dfe2e5; }
        img { max-width: 100%; box-shadow: 0 4px 10px rgba(0,0,0,0.1); border-radius: 8px; margin: 20px 0; }
        ul { padding-left: 2em; }
        table { border-collapse: collapse; width: 100%; margin: 20px 0; }
        th, td { border: 1px solid #dfe2e5; padding: 6px 13px; }
        th { background-color: #f6f8fa; text-align: left; }
        .highlight { color: #d73a49; font-weight: bold; }
        .success { color: #22863a; font-weight: bold; }
    </style>
</head>
<body>

    <h1>👾 PixelNav Station (V28.0 紧急修复版)</h1>

    <blockquote>
        <p><strong>极简、复古、Web3 风格的单文件导航站生成器。</strong><br>
        <em>无需数据库，无需服务器后台，一个 HTML 文件即是一切。</em></p>
    </blockquote>

    <h2>🚨 V28.0 版本更新日志 (Critical Fixes)</h2>
    <p>此版本重点修复了 <strong>批量导入</strong> 和 <strong>移动端交互</strong> 的严重 Bug，建议所有旧版本用户立即升级。</p>

    <h3>✅ 核心修复</h3>
    <ul>
        <li><strong>📥 导入功能重构</strong>
            <ul>
                <li><strong>修复下拉菜单空白</strong>：修复了打开导入窗口时，目标文件夹列表未正确生成的问题。</li>
                <li><strong>智能兜底</strong>：如果当前未选中任何文件夹，系统会自动定位到第一个可用分类，不再报错。</li>
                <li><strong>空状态保护</strong>：如果连一个二级分类都没有，点击导入会直接弹出提示“请先新建分类”，防止程序卡死。</li>
            </ul>
        </li>
        <li><strong>🛡️ 弹窗层级冲突 (Z-Index)</strong>
            <ul>
                <li>修复了“导入窗口”与“错误提示”打架的问题。现在错误提示永远在最顶层，不会导致界面冻结。</li>
            </ul>
        </li>
        <li><strong>📱 移动端/iOS 适配</strong>
            <ul>
                <li>优化了下拉选择框在 iPhone 上的显示样式。</li>
                <li>增加了弹窗的安全边距，防止被软键盘遮挡。</li>
            </ul>
        </li>
    </ul>

    <hr>

    <h2>✨ 核心特性</h2>
    <ol>
        <li><strong>💾 单文件架构 (Serverless)</strong>
            <ul>
                <li>无需数据库，无需后端语言（PHP/Python/Node.js）。</li>
                <li>数据直接“刻录”在 HTML 文件内部，即插即用。</li>
                <li><strong>部署只需一步</strong>：把 HTML 文件上传到 GitHub Pages、Vercel 或任何服务器即可。</li>
            </ul>
        </li>
        <li><strong>🎨 纯正 Windows 98 风</strong>
            <ul>
                <li>经典的灰阶界面、蓝天渐变标题栏、复古滚动条。</li>
                <li>左侧侧边栏文字完美垂直居中。</li>
            </ul>
        </li>
        <li><strong>🔃 稳定的排序系统</strong>
            <ul>
                <li>点击 <strong>排序 (Sort)</strong> 按钮进入专用模式。</li>
                <li>使用 <strong>⬆⬇ 箭头</strong> 进行移动，比拖拽更精准，绝无误触。</li>
            </ul>
        </li>
        <li><strong>📝 强大的批量导入</strong>
            <ul>
                <li>支持 <code>名称 | 网址 | 描述</code> 格式。</li>
                <li>支持直接从 <strong>Excel</strong> 复制粘贴（自动识别制表符）。</li>
                <li>支持粘贴纯网址（自动补全标题）。</li>
            </ul>
        </li>
        <li><strong>🔐 安全与隐私</strong>
            <ul>
                <li>管理员密码采用 <strong>SHA-256</strong> 哈希存储，源码不含明文。</li>
                <li>登录界面移除“默认密码”提示。</li>
            </ul>
        </li>
    </ol>

    <hr>

    <h2>📖 快速上手指南</h2>

    <h3>1. 启动与登录</h3>
    <ol>
        <li>下载 <code>index.html</code> 文件。</li>
        <li>双击直接在浏览器打开。</li>
        <li>点击左下角 <strong>Start</strong> -&gt; <strong>管理员登录</strong>。</li>
        <li>默认密码：<code>admin</code></li>
    </ol>

    <h3>2. 构建您的导航站</h3>
    <ul>
        <li><strong>新建组/文件夹</strong>：点击工具栏的 <code>📂+</code> 图标。<br>
            <em>*提示：建议先建一个“一级大类”，再建“二级文件夹”。</em>
        </li>
        <li><strong>添加链接</strong>：选中一个文件夹，点击 <code>🔗+</code> 图标。</li>
        <li><strong>批量导入</strong>：点击 <code>📝+</code> 图标，粘贴您的网址列表。</li>
    </ul>

    <h3>3. 保存与发布 (重要！)</h3>
    <ul>
        <li>修改完成后，<strong>务必点击工具栏最左侧的 "💾 导出" 按钮</strong>。</li>
        <li>浏览器会下载一个新的 <code>index.html</code>。</li>
        <li><strong>用这个新文件覆盖您服务器上的旧文件</strong>，即完成更新。</li>
    </ul>

    <hr>

    <h2>🛠️ 高级配置</h2>
    <p>点击工具栏的 <strong>⚙️ 设置</strong> 图标，可以自定义：</p>

    <table>
        <thead>
            <tr>
                <th>配置项</th>
                <th>说明</th>
                <th>示例</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><strong>窗口标题</strong></td>
                <td>浏览器标签页显示的文字</td>
                <td><code>我的 Web3 基地</code></td>
            </tr>
            <tr>
                <td><strong>菜单栏</strong></td>
                <td>格式为 <code>名称|链接</code>，逗号分隔</td>
                <td><code>首页|/, 关于|https://github.com</code></td>
            </tr>
            <tr>
                <td><strong>起始时间</strong></td>
                <td>设置建站时间，用于底部读秒</td>
                <td><code>2023-01-01T00:00</code></td>
            </tr>
            <tr>
                <td><strong>状态前缀</strong></td>
                <td>底部状态栏的提示语</td>
                <td><code>系统安全运行</code></td>
            </tr>
        </tbody>
    </table>

    <hr>

    <h2>🔒 如何修改密码？</h2>
    <p>默认密码是 <code>admin</code>。如果您想修改：</p>
    <ol>
        <li>使用 <a href="https://www.google.com/search?q=sha256+online" target="_blank">SHA-256 在线工具</a> 生成您新密码的哈希值。</li>
        <li>用记事本或代码编辑器打开 <code>index.html</code>。</li>
        <li>搜索关键词：<code>const ADMIN_HASH_SHA256</code>。</li>
        <li>将引号内的乱码替换为您生成的新哈希值。</li>
        <li>保存文件。</li>
    </ol>

    <hr>

    <h2>❓ 常见问题 (FAQ)</h2>

    <p><strong>Q: 为什么点击导入按钮没反应？</strong><br>
    A: 请确保您使用的是 <strong>V28.0</strong> 及以上版本。旧版本可能因为未选中文件夹而报错。新版本会自动修复此问题。</p>

    <p><strong>Q: 为什么在手机上有些按钮点不动？</strong><br>
    A: V28.0 已修复移动端层级问题。如果仍有问题，请尝试刷新页面或清除浏览器缓存。</p>

    <p><strong>Q: 部署后数据会丢吗？</strong><br>
    A: 不会。只要您每次修改后都点击了 <strong>"导出"</strong> 并上传了新文件，数据就永久保存在 HTML 代码里了。</p>

    <hr>
    <p><em>Made with ❤️ by PixelNav Team.</em></p>

</body>
</html>

