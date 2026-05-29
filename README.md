# AI Chat Dock

一个纯前端 OpenAI 兼容 AI 聊天网站。

## 功能

- 输入 API Key 与 API 主机地址
- 自动请求 `/v1/models` 获取模型列表
- 选择主对话模型
- 单独选择图片识别模型
- 上传图片后，先用图片识别模型生成说明，再交给主对话模型继续回答
- 移动端自适应
- 本机保存设置
- 导出对话记录

## 使用方式

1. 打开 `index.html`。
2. 填写 API 主机地址，例如：
   - `https://api.openai.com`
   - `https://openrouter.ai/api`
   - 其他 OpenAI 兼容 API 主机
3. 填写 API Key。
4. 点击“获取模型”。
5. 分别选择主对话模型与图片识别模型。
6. 开始聊天。

## 部署到 GitHub Pages

进入仓库：

```text
Settings → Pages → Build and deployment
```

选择：

```text
Source: Deploy from a branch
Branch: main
Folder: /root
```

保存后等待 GitHub 部署完成。

如果仓库名是 `aitest2`，网站地址通常是：

```text
https://izowifar074-bot.github.io/aitest2/
```

## 注意

这是纯前端网页，API Key 只保存在用户自己的浏览器 localStorage 中。不要把自己的 API Key 写死在代码里上传。

如果接口报 CORS 错误，说明该 API 主机不允许浏览器直接跨域请求。此时需要：

- 换支持浏览器跨域的 API 主机；或
- 后续增加一个后端代理。
