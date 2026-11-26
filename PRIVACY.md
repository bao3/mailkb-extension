# Privacy Policy / 隐私政策

**App Name / 应用名称**: MailKB AI (`com.bao3.MailKBAI`)  
**Last Updated / 更新日期**: 2026-11-25

---

## 中文版（简体中文）

MailKB AI 是一款遵循 macOS App Sandbox（应用沙盒）机制设计的本地优先（Local-First）Apple Mail 邮件辅助扩展与桌面伴侣应用。我们高度重视您的邮件隐私与商业数据安全。

### 1. 我们不收集您的任何个人数据
- **无开发者后台服务器**：MailKB AI 不运营任何远程业务服务器、数据采集服务器或行为埋点服务。
- **无广告与追踪**：本应用不包含任何第三方广告 SDK、统计分析 SDK 或崩溃上报追踪组件，也不会跨应用、跨网站追踪您的活动。
- **App Store 隐私标签说明**：开发者不收集（Data Not Collected）您的邮件正文、联系人、附件或使用记录。

### 2. 本地优先与沙盒隔离运行
- **本地知识库与索引（`mailkb_db`）**：`.mbox` / `.eml` 导出邮件及您授权的本地文档目录索引、全文检索、签名与套话自动学习全部在您 Mac 本机的 App Sandbox 与 App Group 沙盒容器内完成，零数据上传。
- **Apple 系统内置离线翻译**：当翻译引擎设为「Apple 内置（完全离线）」或断网自动回退至系统翻译时，译文处理完全在您的设备本地完成。
- **零全局磁盘扫描**：本应用不会申请「完全磁盘访问权限」，也不会直接读取系统邮件私有目录 `~/Library/Mail`，所有导入或归档目录均严格由您通过系统文件选择器主动授权。

### 3. 用户自备 AI 服务说明（BYOK）
- MailKB AI 支持您自行配置外部云端 AI 服务（如 Vertex AI、Gemini API、Anthropic Claude、OpenAI 兼容网关）或您自己搭建的局域网本地推理服务（如 Ollama、vLLM）。
- **仅在主动触发且已配置模型时传输**：只有在您填写了模型配置并点击 AI 摘要、双语回复、或领域规则包建模时，经过正文与签名裁剪后的必要文本才会直接从您的 Mac 发往您指定的模型接口，不经过任何开发者中转服务器。
- **用户完全掌控**：您可以随时清空模型配置、切换至局域网本地模型，或仅使用离线 Apple 翻译与本地知识库检索。发送给第三方模型服务商的数据受该服务商隐私条款约束。
- **凭据加密存储**：您填写的 API Key 仅加密保存在您本机的 macOS 钥匙串（Keychain）中。

### 4. 系统权限用途
- **用户自选文件与安全书签（Security-Scoped Bookmarks）**：仅用于读取您授权索引的 `.mbox` / `.eml` / 业务资料目录，以及向您指定的工作目录保存邮件附件。
- **提醒事项 / 日历权限（EventKit）**：仅在您主动点击「添加到提醒事项」时，将对应邮件待办写入系统「提醒事项」。
- **本地网络权限（Local Network）**：仅在您配置了局域网（RFC1918 或 `.local`）AI 网关时，由宿主应用替扩展完成本地 HTTP 代理转发。

### 5. 数据留存与删除
- 所有本地索引数据库、缓存、分析记录与偏好设置均只存储在您本机的沙盒与 App Group 容器内。
- 您可以随时在应用内删除索引数据、在 macOS「钥匙串访问」中删除 API Key，或直接卸载应用以移除本地应用数据。

### 6. 联系与支持
如对本隐私政策或数据处理方式有任何疑问，请在发布上架前联系开发者支持通道：
- **支持邮箱 / Support Email**: `<填写您的联系邮箱，例如 support@example.com>`
- **项目主页 / Project URL**: `<填写您的开源仓库或官方支持页面链接>`

---

## English Version

MailKB AI (`com.bao3.MailKBAI`) is a local-first macOS MailKit extension and companion host application operating strictly within the macOS App Sandbox.

### 1. Data Not Collected by the Developer
- **No Developer Backend**: MailKB AI operates no developer-hosted servers, telemetry pipelines, or remote analytics services.
- **No Tracking or Ads**: The application contains no third-party advertising SDKs, behavioral trackers, or cross-app tracking identifiers.
- **No Data Collection**: The developer does not collect, store, sell, or share your emails, contacts, attachments, credentials, or usage activity.

### 2. Local-First Processing & App Sandbox
- **Local Knowledge Base (`mailkb_db`)**: Email archive indexing (`.mbox` / `.eml`), authorized workspace document indexing, full-text search, and boilerplate/signature learning run locally inside the macOS App Sandbox and App Group container.
- **On-Device Apple Translation**: When configured to use Apple's built-in translation (or when automatically falling back offline), translation is performed on-device without sending email text to third-party AI APIs.
- **Strict File Access Boundaries**: MailKB AI never requests Full Disk Access and never reads `~/Library/Mail` directly. Folder access is limited strictly to directories you explicitly grant through macOS system file pickers and security-scoped bookmarks.

### 3. User-Configured AI Services (Bring Your Own Key)
- You may optionally configure your own cloud AI provider (such as Vertex AI, Gemini API, Anthropic Claude, or an OpenAI-compatible endpoint) or a self-hosted local network gateway (such as Ollama or vLLM).
- **Explicit Transmission Only**: Trimmed, relevant email context is sent directly from your Mac to your chosen endpoint only when you configure a provider and invoke AI analysis, bilingual reply drafting, or domain pack synthesis. No traffic passes through any developer server.
- **Full User Control**: You can disable cloud AI at any time, route requests strictly to a local LAN model, or use offline Apple Translation and local knowledge base search exclusively. Requests sent to third-party AI providers are governed by those providers' privacy terms.
- **Credential Storage**: API keys are stored locally in the macOS Keychain.

### 4. System Permissions Usage
- **User-Selected Files & Bookmarks**: Used solely to read mail archives/reference directories you select and to file email attachments into your chosen destination folders.
- **Reminders / Calendar (EventKit)**: Used solely when you explicitly choose to add an extracted action item to Apple Reminders.
- **Local Network**: Used solely to connect to user-configured LAN AI inference endpoints via the sandboxed host app loopback relay.

### 5. Data Retention & Deletion
- All indexes, cached summaries, and preferences remain locally on your Mac inside the App Sandbox and App Group container.
- You may remove indexed data or clear API keys in macOS Keychain Access at any time, or uninstall the app to remove local app data.

### 6. Contact
Before submitting to the Mac App Store, publish this document at an HTTPS URL and fill in your active contact details below:
- **Support Email**: `<your-support-email@example.com>`
- **Support URL**: `<https://your-support-url.example>`
