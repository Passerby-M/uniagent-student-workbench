# UniAgent

“基于 Agent 的大学生综合工作台系统的设计与实现”本科毕业设计项目。

当前阶段以课题规划和系统设计为主，暂不扩展业务代码。系统采用“Agent 交互与任务协助 + 工作流可靠执行”的双层结构：Agent 负责事项识别、制度检索、对话式填表、材料预审和流程解释；Flowable 负责正式提交后的任务分配、审批流转、状态管理和审计留痕。

## 当前研究范围

- 深度流程：学生请假与销假；
- 重点 Agent 场景：奖助学金政策解释、资格初筛和材料检查；
- 模板业务：证明申请、学生活动与场地申请；
- 控制原则：关键操作二次确认、工具白名单、资源级鉴权、全程审计、模型故障可降级。

## 技术路线

- 前端：Vue 3、TypeScript、Vite、Element Plus、Pinia；
- 后端：Java 21、Spring Boot 3、Spring Security、Spring Data JPA；
- 工作流：Flowable 7、BPMN 2.0；
- 数据库：H2（开发）、PostgreSQL（部署与实验）；
- Agent：OpenAI 兼容 API、结构化工具调用、RAG；
- 部署：Docker Compose。

## 文档入口

- `docs/01-课题规划.md`：研究定位、业务范围、Agent 能力和实验方向；
- `docs/02-课题设计.md`：双层架构、流程、工具、安全、数据与实验设计；
- `docs/03-开题报告.md`：旧版报告停用说明，正式报告将在设计稳定后重写。

## 本地要求

- Java 21
- Maven 3.9+
- Node.js 22+
- Docker

## 后端验证

```bash
mvn test
```

默认使用内存 H2 数据库。模型配置通过 `AI_API_KEY`、`AI_BASE_URL` 和 `AI_MODEL` 环境变量注入，未配置时使用 Mock 或关闭 Agent，不影响工作流基础功能。
