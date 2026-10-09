# 安装、更新与回退

运行环境：能够加载 SKILL.md 和读取随包 Markdown/DOCX 的 AI 助手。主要在 Codex 使用；其他宿主未经本次实测。无 Python、Node、外部 MCP、API Key 或自动通知服务依赖。官方 DOCX可由支持 OOXML 的阅读器读取，不必调用 Word 或 LibreOffice。

1. 解压候选 ZIP。打开 gdpr-data-breach-triage-v0.1.2 目录。
2. 如已有同名 Skill，先将它备份至 Skills 目录之外。
3. 将其中 gdpr-data-breach-triage 文件夹完整复制到 Codex Skills 目录；默认是 ~/.codex/skills/，自定义 CODEX_HOME 时使用其 skills/ 目录。请勿仅复制 SKILL.md，也勿把外层发布文档目录当作 Skill 安装。
4. 开启新会话，用 README 中的示例调用。若未出现，核对文件夹层级和宿主当前的 Skill 发现设置。
5. 检查安装后的 assets/、references/、agents/、LICENSE 和 THIRD_PARTY_NOTICES.md 均存在。

更新前备份旧目录；整目录替换，避免残留旧模板。卸载时移出同名目录；回退时恢复备份并开启新会话。Skill 不存储案件账本、不提交表单；删除它不会删除宿主聊天记录或用户另存的事件材料。

本次仅在临时目录完成解压及结构/身份检查，没有替换维护者的本机安装，也没有实际启动另一宿主会话。
