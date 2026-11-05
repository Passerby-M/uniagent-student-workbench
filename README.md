# FacultyFlow

“基于工作流的高校教师综合工作台系统”本科毕业设计项目。

当前阶段：完成课题范围、技术路线和基础目录，正在实现第一个“申请—审批—归档”闭环。

## 本地要求

- Java 21
- Maven 3.9+
- Node.js 22+
- Docker（部署 PostgreSQL 时使用）

## 后端启动

```bash
mvn -pl backend spring-boot:run
```

默认使用内存 H2 数据库，不需要预先配置 PostgreSQL。大模型密钥通过 `AI_API_KEY` 环境变量注入，未配置时后续使用 Mock 实现。

## 前端启动

```bash
cd frontend
npm install
npm run dev
```

详细设计见 `docs/01-课题规划.md`。
