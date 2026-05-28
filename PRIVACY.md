# Privacy Policy — Cross-Tab Semantic Search

**Effective date: 2026-05-28**

Cross-Tab Semantic Search ("the Extension") is designed to be **local-first**. This
policy explains exactly what the Extension does and does not do with your data.

## Summary

- All page content, text segments, vectors, and search indexes are stored **only in
  your browser's local IndexedDB**. Nothing is uploaded to us or any third party.
- The Extension has **no backend server** and collects **no analytics**.
- The only outbound network request is a one-time download of the open-source
  embedding model files from `huggingface.co`. This request contains **none of your
  browsing data** — it only fetches the model.

## What data the Extension processes

To provide semantic search, when you visit an http/https page the Extension:

1. Extracts the page's main text content (using Mozilla Readability), in the page tab.
2. Splits that text into segments and converts each into a numeric vector ("embedding")
   using a machine-learning model that runs **entirely inside your browser**.
3. Stores the following **locally** in IndexedDB:
   - Page URL (without the `#fragment`), page title, and host
   - The extracted text segments
   - The corresponding embedding vectors
   - A timestamp and a content hash (to detect changes / avoid re-indexing)

When you search, your query is converted to a vector locally and compared against the
stored vectors on your device. Your query never leaves your browser.

## Where data is stored

- **Locally only**, in your browser's IndexedDB, on your device.
- The Extension does not sync, back up, or transmit this data anywhere.

## Network requests

- **Model files:** On first use, the embedding model weights and tokenizer are
  downloaded from `https://huggingface.co` (and its CDN hosts under `*.hf.co`) and then
  cached by your browser. This is a request for static model files; it does **not**
  include your URLs, page content, queries, or any personal data.
- The ONNX runtime (WebAssembly) is **bundled inside the Extension** and runs locally.
- No other network requests are made.

## Data you control

- **Retention:** Indexed pages older than your configured retention period (default
  30 days) are automatically removed.
- **Blocklist:** You can exclude any host from being indexed.
- **Auto-index toggle:** You can turn off automatic indexing entirely.
- **Clear all data:** You can permanently delete all indexed pages and vectors at any
  time from the Settings panel.
- Built-in browser pages (`chrome://`, `chrome-extension://`, `file://`, `about:`,
  `view-source:`, etc.) are never indexed.

## Data sharing

We do **not** sell, transfer, or share your data with anyone. We never receive your
data in the first place, because it stays on your device.

## Permissions

The Extension requests broad host access (`<all_urls>`) solely so it can read page
content on the sites you visit and index them for your own local search. It does not
use this access for any other purpose.

## Changes to this policy

If this policy changes, the updated version will be published at this URL with a new
effective date.

## Contact

Questions about this policy: **[your-contact-email]**

---

# 隐私政策 — 跨标签页语义搜索

**生效日期：2026-05-28**

"跨标签页语义搜索"（下称"本扩展"）秉持**本地优先**原则。本政策准确说明本扩展对你的数据
做了什么、没做什么。

## 概要

- 所有网页内容、文本片段、向量与搜索索引**仅保存在你浏览器本地的 IndexedDB**，不会上传到
  我们或任何第三方。
- 本扩展**没有后端服务器**，**不收集任何分析数据**。
- 唯一的对外网络请求，是首次使用时从 `huggingface.co` 下载开源嵌入模型文件。该请求**不包含
  你的任何浏览数据**，仅用于获取模型。

## 本扩展处理哪些数据

为实现语义搜索，当你访问 http/https 网页时，本扩展会：

1. 在该网页标签页内，使用 Mozilla Readability 抽取网页正文。
2. 将正文切分为片段，并用**完全在你浏览器内运行**的机器学习模型，把每个片段转成数值向量
   （"嵌入"）。
3. 将以下内容**保存在本地** IndexedDB：
   - 网页 URL（去掉 `#` 锚点）、标题、主机名
   - 抽取出的文本片段
   - 对应的嵌入向量
   - 时间戳与内容哈希（用于检测变化、避免重复索引）

搜索时，你的查询在本地转成向量，并与设备上已存的向量比较。**你的查询不会离开浏览器。**

## 数据存储位置

- **仅本地**，保存在你设备上浏览器的 IndexedDB 中。
- 本扩展不会同步、备份或向任何地方传输这些数据。

## 网络请求

- **模型文件：** 首次使用时，从 `https://huggingface.co`（及其 `*.hf.co` CDN 主机）下载嵌入
  模型权重与分词器，之后由浏览器缓存。这是对静态模型文件的请求，**不包含**你的 URL、网页
  内容、查询或任何个人数据。
- ONNX 运行时（WebAssembly）**已打包在扩展内部**，本地运行。
- 不发起任何其他网络请求。

## 你可控制的数据

- **保留期：** 超过你设定保留天数（默认 30 天）的已索引页面会被自动清除。
- **黑名单：** 可排除任意主机不被索引。
- **自动索引开关：** 可完全关闭自动索引。
- **清空全部数据：** 可随时在设置面板永久删除所有已索引页面与向量。
- 浏览器内置页面（`chrome://`、`chrome-extension://`、`file://`、`about:`、`view-source:`
  等）永远不会被索引。

## 数据共享

我们**不会**出售、转移或与任何人共享你的数据。由于数据始终留在你的设备上，我们根本不会
接触到你的数据。

## 权限

本扩展请求广泛主机访问权限（`<all_urls>`），仅用于读取你访问网站的网页内容并为你的本地搜索
建立索引，绝不用于任何其他目的。

## 政策变更

若本政策变更，更新版本将发布于本 URL 并标注新的生效日期。

## 联系方式

关于本政策的疑问：**[你的联系邮箱]**
