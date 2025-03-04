# RPA_Project
My First RPA project, See how it works !!!
## Day 1 20240303
RPA stands for Robotic Process Automation, it sounds interesting.
After watchiing so many videos, firstly, I noticed that most of them are created by indian and Most rpa tools are none-programing based. It only need you to drag and drop some parts of its components. I also noticed a web recorder which is very useful in real life indeed.
### Open source project
Most of tools are commential software aimed for industry company. I still finded some open soure ones.
### Conclusion
A very useful tool to boost the daily work of all employees !!!
### day2
Detailed instructions:

 1. 需求分析与流程定义
- 目标：明确自动化范围和可行性。
  - 识别重复性高、规则明确、结构化输入/输出的业务流程。
  - 收集流程文档（如操作手册、系统截图、数据样例）。
  - 评估技术可行性（例如系统是否支持自动化操作，如是否有 API、UI 元素是否可识别）。
- 输出：需求文档（Process Definition Document, PDD）或用户故事（Agile 开发）。

---

 2. 流程设计与架构规划
- 流程图绘制：
  - 使用 UiPath Studio 的流程图工具或第三方工具（如 Visio）绘制详细流程图。
  - 明确逻辑分支、异常处理、数据输入/输出点。
- 技术设计：
  - 选择自动化模式（前台操作 vs. 后台操作、Attended vs. Unattended Robot）。
  - 确定依赖项（如 Excel、数据库、API、第三方库）。
  - 规划异常处理策略（重试机制、日志记录、通知）。
- 输出：技术设计文档（Solution Design Document, SDD）。

---

 3. 开发阶段
- UiPath Studio 开发：
  - 活动（Activities）拖放：使用内置活动（如 `Click`、`Type Into`、`Read PDF`）或自定义代码（C/VB）。
  - 数据操作：通过变量（Variables）、参数（Arguments）、数据表（DataTables）管理流程数据。
  - 选择器（Selectors）配置：确保 UI 元素可稳定识别（使用通配符、锚点、OCR 等）。
  - 异常处理：使用 `Try Catch`、`Retry Scope` 和 `Global Exception Handler`。
  - 日志与监控：通过 `Log Message` 和 `Orchestrator` 集成记录执行状态。
- 版本控制：
  - 使用 Git 或 UiPath 内置的版本管理工具（Projects.json）管理代码。
- 输出：`.xaml` 工作流文件、依赖的库（如 `.nupkg` 包）。

---

 4. 测试与调试
- 单元测试：
  - 在 Studio 中通过调试工具（如 `Debug` 模式、断点）验证单个步骤。
- 集成测试：
  - 模拟真实环境数据，测试端到端流程。
  - 验证异常场景（如系统延迟、数据错误、权限问题）。
- 用户验收测试（UAT）：
  - 与业务用户协作，确认流程符合需求。
- 输出：测试报告、缺陷跟踪记录。

---

 5. 部署与调度
- 发布到 Orchestrator：
  - 将流程打包为 `.nupkg` 并上传到 UiPath Orchestrator。
  - 配置流程参数（如输入参数、环境变量）。
- 机器人调度：
  - 为 Unattended Robot 创建作业（Jobs），设置触发条件（定时、事件触发或手动触发）。
  - 分配机器人资源（如机器池、负载均衡）。
- 权限管理：
  - 在 Orchestrator 中配置角色、文件夹权限和机器人访问控制。
- 输出：Orchestrator 中的流程部署完成，机器人可执行任务。

---

 6. 监控与维护
- 实时监控：
  - 通过 Orchestrator 仪表板查看作业状态、执行日志和机器人负载。
  - 设置警报（如流程失败、执行超时）。
- 异常处理：
  - 分析日志，修复流程中的缺陷或优化性能。
  - 更新版本并重新发布到 Orchestrator。
- 持续优化：
  - 根据业务变化调整流程（如系统升级、规则变更）。
  - 定期审查自动化 ROI（节省时间、错误率降低等）。

---

 7. 文档与知识转移
- 技术文档：
  - 编写操作手册（Runbook），包含部署步骤、维护指南。
- 用户培训：
  - 培训业务用户使用 Attended Robot（如手动触发流程）或处理异常。
- 知识库：
  - 在团队内共享最佳实践和常见问题解决方案。

---

 关键工具与组件
1. UiPath Studio：开发自动化流程的核心 IDE。
2. UiPath Robot：执行自动化任务的本地或云端机器人。
3. Orchestrator：集中管理机器人、流程和调度。
4. UiPath Assistant：用户与机器人交互的桌面客户端（用于 Attended Automation）。
5. AI Center（可选）：集成 AI/ML 模型处理复杂场景（如文档分类、NLP）。

---

 典型项目生命周期示例
plaintext
需求收集 → 流程设计 → 开发 → 本地测试 → UAT → 部署到生产 → 监控 → 维护/优化

通过以上流程，UiPath 能够实现从需求到生产的高效自动化，同时确保流程的稳定性和可维护性。
