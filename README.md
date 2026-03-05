# CryptoFolio 💹

> 加密资产 & 投资组合管理工具 · 纯前端 · 零依赖 · 本地数据

**🔗 在线访问：** `https://你的用户名.github.io/cryptofolio/`

---

## 功能

- **总览** — 资产总值、资金分布、最近交易一览
- **持仓** — 行内直接编辑，价值实时联动（价格 × 数量），支持排序和备注
- **交易** — 记录买卖方向、价格、盈亏
- **理财** — 支持 USD 计价和币本位，APY 自动每日计算收益
- **账户** — 点击卡片查看持仓详情，支持直接添加/编辑/删除资产
- **AI 录入** — 用自然语言或截图描述交易，自动解析保存
- **实时价格** — 一键刷新，自动拉取 CoinGecko 行情
- **Notion CSV 导入** — 直接导入 Notion 数据库导出的持仓数据

---

## 使用方式

### 方式一：直接下载使用（本地离线）
下载 `index.html`，双击用 Chrome / Edge 打开即可。无需安装任何依赖。

### 方式二：GitHub Pages 在线访问
Fork 本仓库，开启 GitHub Pages 即可获得公开链接。

---

## AI 录入配置

AI 功能需要填入 API Key（存储在本地浏览器，不上传）。

点击右上角 **「设置 AI」** 按钮，选择模型并填入 Key：

| 模型 | 获取地址 | 图片识别 | 本地HTML可用 |
|------|---------|---------|------------|
| **Claude（推荐）** | [console.anthropic.com](https://console.anthropic.com) | ✅ | ✅ |
| OpenAI / GPT | [platform.openai.com](https://platform.openai.com) | ✅ | GitHub Pages 可用 |
| DeepSeek | [platform.deepseek.com](https://platform.deepseek.com) | ❌ | GitHub Pages 可用 |
| MiniMax | [platform.minimaxi.com](https://platform.minimaxi.com) | ❌ | GitHub Pages 可用 |

> 从本地 `file://` 打开时，只有 Claude API 支持直接调用。部署到 GitHub Pages 后，其他模型也可正常使用。

---

## 数据说明

- 所有数据存储在**浏览器本地 localStorage**，不上传任何服务器
- 不同设备/浏览器之间数据不同步
- 清除浏览器缓存会丢失数据，建议定期导出备份

---

## 技术栈

纯原生 HTML + CSS + JavaScript，零外部依赖，单文件即完整应用。

- 价格数据来自 [CoinGecko](https://coingecko.com) 免费 API
- AI 功能通过用户自己的 API Key 调用对应模型
