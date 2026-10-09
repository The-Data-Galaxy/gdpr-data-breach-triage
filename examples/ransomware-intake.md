# 合成案例：勒索事件的四轮分诊与通知草稿

方法：2026-10-09，主 Agent 根据固定 R02 四轮输入和最终候选模板，生成并人工式自评的 artifact-assisted replay。无独立执行器、无盲测；此输出不是2026年7月缺失记录的恢复。以下所有事件事实均为合成材料。

## Turn 1 — 用户

我们收到了勒索邮件，说我们的服务器被锁定了，访问不了用户数据了，我们是否需要做数据泄露通知？

## Turn 1 — 助手

可能存在可用性受损的个人数据泄露；通知结论仍需关键事实。

**已记录**

- 已确认：收到勒索邮件，邮件声称服务器被锁定。
- 已确认：目前无法访问用户数据。
- 未知：组织角色、控制者知悉时间、数据范围及外泄证据。

**请按编号回复**

1. 你们对这些数据是控制者、处理者，还是角色尚不明确？这决定通知职责，可向隐私或合同负责人核对。
2. 何时首次收到警报，何时确认个人数据确受影响？请提供时间及时区，便于区分T0/T1，可核对工单与日志。
3. 涉及哪些个人数据，受影响范围目前能估计多少？这影响风险，可查系统负责人记录。
4. 目前已知的外泄迹象、攻击者访问及恢复情况是什么？请只报告已确认信息，可向安全团队核对。

## Turn 2 — 用户

我们是控制者。

## Turn 2 — 助手

控制者身份已记录，第33条与第34条的通知判断由你们负责。

**已记录**

- 已确认：你们是控制者，收到勒索邮件，当前无法访问用户数据。
- 未知：控制者知悉时间、具体数据和范围、外泄及恢复证据。

**请继续确认**

1. 请提供首次警报与确认个人数据受影响的时间及时区；可核对工单/日志，确定T1与可能的72小时期限。
2. 目前确认涉及哪些用户数据、业务影响和可恢复情况？可由系统/安全负责人说明，以判断可用性损失的风险。

## Turn 3 — 用户

有用户订单信息，当前无法确定是否对外泄露了、现在服务不可用了。48小时前就无法访问了。

## Turn 3 — 助手

订单信息和持续48小时无法访问已记录。若48小时前也是控制者达到合理确定发生个人数据泄露的T1，则72小时窗口可能仅剩约24小时；停机开始本身不能自动确定T1。现在进入及时通知准备路径，不等待完整取证。

### GDPR 数据泄露初判卡

#### 1. 初步结论

- 组织角色：控制者（已确认）。
- 是否构成个人数据泄露：Likely personal data breach；用户订单数据持续无法访问，可能构成可用性泄露。
- 监管机构通知判断：准备分阶段通知。持续服务中断及订单数据不可访问使风险尚不能排除，应立即由隐私/DPO/法务复核第33条门槛，必要时先提交已有信息后补充。
- 数据主体告知判断：现有事实不足以认定高风险；立即复核中断对个人的实际后果、数据敏感度及外泄迹象，不把监管通知建议自动等同于第34条告知义务。
- 结论可信度：中；可用性事实明确，影响范围及T1不明。
- 人工复核要求：以上为初步决策支持，外部行动前由隐私团队、DPO、法务或获授权控制者代表确认。

#### 2. 关键时间

- T0 初始警报：收到勒索邮件，具体时间未知。
- T1 控制者知悉：未知；需确认何时达到合理确定个人数据泄露的程度。
- 72小时截止时间：不能计算绝对时刻。若T1确在48小时前，则可能约剩24小时；还需时间戳及时区。
- 时间依据：用户陈述48小时前即无法访问，并非日志证明T1。
- 时间不确定性：首次报警、个人数据影响确认与停机开始可能不同。

#### 3. 已知事实

- 事件：收到勒索邮件，邮件称服务器锁定；服务不可用。
- 泄露性质：可用性受损；保密性外泄未知；完整性变化未知。
- 数据类别：用户订单信息，具体字段未知。
- 数据主体及人数：涉及用户；人数、是否有脆弱群体未知。
- 接触方或攻击者：勒索邮件发件人身份及实际访问权限未知。
- 已采取措施：未知，不假定已隔离、恢复或加密。

#### 4. 风险判断

- 风险增加因素：服务及订单数据持续48小时不可访问，可能影响个人交易或相关权益；外泄和后续访问未排除。
- 风险降低因素：目前没有已确认的有效减轻措施。可核实备份和恢复能力，不能将其假定为已生效。
- 证据状态：以上均为用户陈述；没有取证日志或独立访问证据。
- 主要潜在后果：交易延误或服务权益受影响，实际严重性未知；外泄导致的后果仅为待核实情形。
- 尚未确认：T1、具体字段/人数、恢复状况、个人后果、外泄证据和主管机关。

#### 5. 未来行动

- 立即：安全团队核对时间线与恢复情况；隐私团队保留事件记录并复核通知门槛。
- 下一复核点：建议立即安排，不把建议时间当作法律截止时间。
- 24小时内：若条件式T1成立，应在实际72小时届满前完成必要首报；不得因资料不全自动延后。
- 48小时内：按确认后的实际期限与首报情况跟进补充，不能把该建议理解为允许再等48小时。
- 72小时前：从支持充分的实际T1起算；需通知时及时通知，确有延迟则说明原因。后续信息不无故拖延。

### 关键缺失信息清单

| 编号 | 待确认事实 | 为什么影响结论 | 建议来源/负责人 | 确认期限 |
| --- | --- | --- | --- | --- |
| 1 | T0、T1的原始时间戳及时区 | 决定通知时限 | 工单、日志、事件负责人 | 建议立即核实 |
| 2 | 订单字段、涉及人数及个人实际后果 | 决定风险与高风险门槛 | 业务、隐私团队 | 建议立即并行核实 |
| 3 | 恢复能力、外泄及攻击者访问证据 | 影响可用性持续损害和保密性风险 | 安全团队、日志 | 建议立即并行核实 |
| 4 | 控制者实体、所在地与跨境处理范围 | 确定主管机关，避免猜测门户 | DPO、法务 | 提交前核实 |

不再重复询问控制者身份、订单信息或已陈述的48小时停机。

## Turn 4 — 用户

请准备提供给数据保护机构的通知。

## Turn 4 — 助手

以下为待复核工作草稿，沿用上轮事实和缺失信息清单。主管机关、控制者实体及实际T1均未确认，因此不填写绝对日期、人数或申报机关。模板采用EDPB 2026 Version 1.0征求意见稿；2026-10-09来源页面显示征求意见已关闭，本核对不证明已定稿或当地实施。需要隐私/DPO/法务或获授权控制者代表确认后才能对外提交。

# EDPB Template for Personal Data Breach Notification — Draft Working Copy

> Use this field order for every supervisory-authority notification draft. It follows the EDPB Version 1.0 consultation DOCX adopted on 08 June 2026. Keep `[TO CONFIRM]` for unknown values and use conditional fields only when their trigger applies.

## 1.  Information on the personal data breach notification [Field 1]

### 1.1  Type of notification [Field 2]

- **3. Type of notification:** [TO CONFIRM] — 拟按 New Notification 准备，提交前核实是否已有首报。
- **4. Sub-type of notification:** [TO CONFIRM] — 当前信息不全，拟按 Incomplete；取决于第3项确认。
- **5. Reasons for withdrawing a previous notification:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **6. ID of previously notified personal data breach:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **7. Data controller's internal reference number:** [TO CONFIRM] — 此字段值及适用条件尚待核实。

## 2.  Identification of the data controller and the reporting person [Field 8]

### 2.1  About the data controller [Field 9]

- **10. Type of Identifier:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **11. Identifier:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **12. Name of the organisation:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **13. Contact details*:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **14. Sector:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **15. Type of organisation:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **16. Further description of organisation type:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **17. Classification of economic activity:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **18. Name of representative in EEA:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **19. Contact details* of representative in EEA:** [TO CONFIRM] — 此字段值及适用条件尚待核实。

### 2.2  Identity of the reporting person [Field 20]

- **21. Name of the reporting person :** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **22. Contact details:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **23. Function of the reporting person :** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **24. Description of the function of the reporting person:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **25. National identification number:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **26. Accuracy & Responsibility:** [TO CONFIRM] — 此字段值及适用条件尚待核实。

### 2.3   Name and contact details of the data protection officer or other contact point where more information can be obtained [Field 27]

#### 2.3.1 About the data protection officer [Field 28]

- **29. Is a data protection officer designated?:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **30. Name of the DPO :** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **31. Contact details*:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
#### 2.3.2 About the contact point where more information can be obtained [Field 32]

- **33. More information about the incident can be obtained at:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **34. Name of the contact person :** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **35. Function of the contact person :** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **36. Contact details*:** [TO CONFIRM] — 此字段值及适用条件尚待核实。

### 2.4 Involvement of other parties [Field 37]

- **38. Are other parties such as data processors or joint controllers involved?:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **39. Qualification of the other involved party:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **40. Name of the other involved party:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **41. Contact details*:** [TO CONFIRM] — 此字段值及适用条件尚待核实。

## 3.  Initial information on the personal data breach   [Field 42]

### 3.1   Date and time of the personal data breach and of its detection [Field 43]

- **44. When did the personal data breach occur?:** To be determined — 已陈述48小时前无法访问，确切起止和时区待确认。
- **45. Only estimated dates are possible:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **46. Beginning date and time of personal data breach:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **47. Ending date and time of personal data breach:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **48. Date and time of awareness of the data controller of the personal data breach:** [TO CONFIRM] — 停机起点不自动等于T1，需核对何时确认个人数据影响。
- **49. Reasons for late notification of the personal data breach:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **50. How was the personal data breach discovered?:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **51. Further description of the discovery of the personal data breach:** 收到勒索邮件，邮件声称服务器被锁定；用户报告服务及用户数据不可访问。
- **52. Date of notification by other party:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **53. Further comments on timeline and additional information:** 用户称48小时前即无法访问；本草稿未获具体时间戳、时区或T1证据。

### 3.2   Nature, circumstances and summary of the personal data breach [Field 54]

- **55. Nature of the personal data breach:** Availability — 保密性外泄和完整性变化尚未确认。
- **56. Type of confidentiality breach:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **57. Was the data unintelligible to anyone who was not authorised to access it  or were individuals not identifiable?:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **58. Type of integrity breach:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **59. Type of availability breach:** Not determined — 当前仍不可用，持续性/可恢复性待核实。
- **60. Nature of the incident:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **61. Cause of the personal data breach:** To be determined — 勒索邮件本身不能证明全部攻击事实或原因。
- **62. Further description of the nature of the incident:** 用户订单信息无法访问，服务不可用；是否对外泄露未知。
- **63. Description of the systems, software, services, and infrastructures involved in the personal data breach and where they are located:** 服务器和订单服务受影响（用户陈述）；[TO CONFIRM] — 软件、基础设施及地点未知。

### 3.3   Categories and number of data subjects concerned [Field 64]

- **65. Categories of concerned data subjects:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **66. Further description of categories of concerned data subjects and additional data subjects:** 涉及用户订单信息；[TO CONFIRM] — 数据主体的具体类别、人数和脆弱群体情况。
- **67. Data subjects concerned by the personal data breach:** To be determined
- **68. Number of data subjects concerned by the personal data breach:** [TO CONFIRM] — 此字段值及适用条件尚待核实。

### 3.4   Categories and number of personal data records concerned [Field 69]

- **70. Type of breached data:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **71. Further description of breached data and additional data categories:** 用户订单信息；[TO CONFIRM] — 具体字段未知，不推定含身份、地址、付款或敏感信息。
- **72. Personal data records concerned by the personal data breach:** To be determined
- **73. Number of personal data records concerned by the personal data breach:** [TO CONFIRM] — 此字段值及适用条件尚待核实。

### 3.5   Measures in place when the personal data breach occurred [Field 74]

- **75. Relevant measures in place when the personal data breach occurred:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **76. Further description of relevant measures in place when the personal data breach occurred:** [TO CONFIRM] — 此字段值及适用条件尚待核实。

## 4.   Further information on the personal data breach [Field 77]

### 4.1   Likely consequences of the personal data breach and potential adverse effects on data subjects [Field 78]

- **79. Likely consequences in case of breach of confidentiality:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **80. Description of other confidentiality consequences:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **81. Likely consequences in case of breach of integrity:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **82. Description of other integrity consequences:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **83. Likely consequences in case of breach of availability :** [TO CONFIRM] — 可能无法获取订单或使用相关服务，个人实际后果待业务团队核实。
- **84. Description of other availability consequences:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **85. Nature of the potential impact for the data subject:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **86. Further description of the other impacts for the data subjects:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **87. Severity of the potential impacts:** To be determined

### 4.2   Assessment of the risk to the rights and freedoms of natural persons [Field 88]

- **89. Outcome of the risk assessment carried out by the controller:** Additional information needed
- **90. Further description  of the risk assessment carried out by the data controller:** 持续48小时的可用性受损使风险尚不能排除，准备分阶段监管通知供人工复核；高风险及第34条沟通另行判断。

### 4.3   Measures taken (or proposed to be taken) to address the personal data breach and to mitigate its possible adverse effects [Field 91]

- **92. Measures taken to address the personal data breach and to mitigate its consequences:** [TO CONFIRM] — 未提供已执行措施；隔离、恢复及保全日志为待核实/拟议行动，不写成已完成。

### 4.4   Measures taken (or proposed to be taken) to prevent similar personal data breach [Field 93]

- **94. Relevant measures taken to prevent similar personal data breach:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **95. Further description of relevant updated permanent measures to avoid similar incidents in the future:** [TO CONFIRM] — 此字段值及适用条件尚待核实。

## 5.   Communication to the data subjects [Field 96]

- **97. Has the personal data breach been communicated to data subjects?:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **98. Date of when information was given to data subjects:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **99. Future date on which the data breach will be communicated to the data subjects:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **100. Further information about conditions referred to in article 34(3) of the GDPR that are met:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **101. Further description why the conditions referred to in article 34(3) of the GDPR that are met and the measures taken:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **102. Number of data subjects informed:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **103. Further description why not all data subjects have been informed:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **104. Means of communication used to inform the data subject:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **105. Further description of the other means of communication:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **106. Content of the information provided to the data subjects:** [TO CONFIRM] — 此字段值及适用条件尚待核实。

## 6.   Possible other issues [Field 107]

### 6.1   Whether other authorities or bodies have been notified [Field 108]

- **109. Has the incident been reported to the police/judicial authorities as a criminal offence?:** Unknown
- **110. Has the incident been notified to other supervisory authorities or control bodies under other relevant legislation? (e.g. national cyber security centre, etc.):** Unknown
- **111. Further information about notification to other authorities or bodies:** [TO CONFIRM] — 此字段值及适用条件尚待核实。

### 6.2   Whether the personal data breach involves a cross-border processing [Field 112]

- **113. Does the personal data breach involve cross-border processing carried  out by a controller established in the European Economic Area (EEA)?:** Unknown
- **114. The lead supervisory authority is::** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **115. List of EEA countries where the controller has an establishment:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **116. List of EEA countries where affected data subjects are located:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **117. Approximate number of data subjects per country:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **118. List of EEA supervisory authority to which the breach has been or will be notified:** [TO CONFIRM] — 此字段值及适用条件尚待核实。

### 6.3   Whether the personal data breach involves a processing at non-EU establishments [Field 119]

- **120. Does the personal data breach involve processing, to which the GDPR applies, carried out by a controller that is not established in the European Economic Area (EEA)?:** Unknown
- **121. List of EEA countries where affected data subjects are located:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **122. Approximate number of data subjects per country:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **123. List of EAA supervisory authority to which the breach has been or will be notified:** [TO CONFIRM] — 此字段值及适用条件尚待核实。

## 7.   Attachments [Field 124]

- **125. Please identify the attachments to this notification:** [TO CONFIRM] — 此字段值及适用条件尚待核实。
- **126. Other attachements:** [TO CONFIRM] — 此字段值及适用条件尚待核实。

字段填写中的待核实不是省略；任何第34(3)例外、通知历史或补救措施均未被假定成立。未执行实际提交。
