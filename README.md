# GDPR 数据泄露分诊与通知准备 Skill

**v0.1.2 早期版本｜2026-10-09 已获人工接受与公开发布授权**

[下载 v0.1.2 ZIP](gdpr-data-breach-triage-v0.1.2.zip) · [批准记录与包身份](PUBLICATION.md)

ZIP 保留批准时的候选快照，包内准备状态措辞对应生成时间；当前批准记录见 PUBLICATION.md。

帮助隐私团队、DPO 和法务把事件材料整理成 GDPR 初步判断：是否可能发生个人数据泄露、何时知悉、是否建议通知监管机构、是否需要向数据主体沟通，以及哪些事实还需确认。

## 能做什么

- 事实不完整时分轮问诊，首轮最多四问，后续通常最多两问。
- 区分初始警报、控制者知悉时间与可能的 72 小时期限。
- 分别评估 GDPR 第33条监管通知与第34条数据主体沟通。
- 按需要交付分诊卡、关键事实清单和 EDPB 字段顺序通知草稿。

## 安装与开始

见 [INSTALL.md](INSTALL.md)。将本仓库 `gdpr-data-breach-triage/` 文件夹复制至 Codex 的 Skills 目录，再在新会话中调用：

> 使用 $gdpr-data-breach-triage。我们是数据控制者，订单系统已无法访问48小时，收到勒索邮件，尚不能确认数据是否被窃取。请先指出关键风险和必须确认的事实。

没有明确知悉时间时，Skill 应保留条件表达，不直接编造截止时刻。完整模拟输入和输出见 [examples/ransomware-intake.md](examples/ransomware-intake.md)。

## 适用边界

仅覆盖 GDPR 初步分诊与通知准备。成员国监管机关流程、具体门户、其他法域、行业通知义务和自动提交不在本版本范围内。结果由隐私团队、DPO、法务或获授权控制者代表复核；不构成最终法律意见或完成申报的证明。

## EDPB 模板状态

使用 EDPB 2026 Version 1.0 征求意见稿，保留官方 Field 1–126 顺序与英文标签。2026-10-09 核对时，官方页面已标注征求意见关闭，仍说明实际实施时间将另行决定；本包不据此声称模板已定稿或被任何具体 DPA 采用。提交前应核对主管机关当前要求。

[模板与状态](https://www.edpb.europa.eu/public-consultations/template-for-personal-data-breach-notification_en) · [EDPB 再利用条件](https://www.edpb.europa.eu/copyright_en)

## 验证范围

历史记录为5个 smoke 案例、35条标准通过，以及R02的7条标准通过。历史R02原始输出缺失。本次保存新的主 Agent 辅助回放与逐字段核验，未进行独立盲测、真实事件验证或门户测试。详见 [VALIDATION.md](VALIDATION.md)，请勿将这些有限证据解释为生产级准确率保证。

## 许可与反馈

原创材料采用 [Apache-2.0](LICENSE)；EDPB 官方 DOCX及其字段改编使用单独来源条件，见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)，不重新许可为 Apache-2.0。

发现问题时，向维护者提供去标识化的最小输入、实际与预期行为、版本及受影响字段。不要提交真实事件原件、个人信息、密钥或安全细节。维护者应先记录失败样本，再做最小修复和定向回归；在仓库 Issues 中报告问题时请遵循同样的去标识化要求。
