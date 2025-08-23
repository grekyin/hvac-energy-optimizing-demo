# Demo项目完整结构说明

## 项目概述

HVAC能源优化系统演示项目是一个用于展览会演示的工业空调节能智能控制系统，采用Docker容器化部署，包含三个核心组件。

## 完整目录结构

```
demo/
├── README.md                           # 项目主说明文档
├── project-structure.md                # 项目结构说明文档
│
├── docs/                               # 文档目录
│   ├── README.md                       # 文档说明
│   ├── api/                            # API文档
│   │   ├── datasource-api.md           # 数据源API文档
│   │   ├── resling-api.md              # Resling应用API文档
│   │   └── frontend-api.md             # 前端API文档
│   ├── user-guide/                     # 用户指南
│   │   ├── demo-operation-guide.md     # 演示操作指南
│   │   ├── user-manual.md              # 用户手册
│   │   └── faq.md                      # 常见问题
│   └── developer-guide/                # 开发者指南
│       ├── development-setup.md        # 开发环境搭建
│       ├── coding-standards.md         # 代码规范
│       ├── development-workflow.md     # 开发流程
│       └── testing-guide.md            # 测试指南
│
├── docker/                             # Docker容器目录
│   ├── README.md                       # Docker说明
│   ├── docker-compose.yml              # 整体编排文件
│   ├── datasource/                     # 数据源容器
│   │   ├── Dockerfile                  # 数据源镜像构建
│   │   ├── docker-compose.yml          # 数据源编排
│   │   ├── init.sql                    # 数据库初始化
│   │   ├── data/                       # 数据文件
│   │   │   ├── historical-data.sql     # 历史数据
│   │   │   └── real-time-data.sql      # 实时数据
│   │   └── config/                     # 配置文件
│   │       └── my.cnf                  # MySQL配置
│   ├── resling-app/                    # Resling应用容器
│   │   ├── Dockerfile                  # Resling应用镜像构建
│   │   ├── docker-compose.yml          # Resling应用编排
│   │   ├── app/                        # 应用代码
│   │   │   ├── package.json            # Node.js依赖
│   │   │   ├── requirements.txt        # Python依赖
│   │   │   └── src/                    # 源代码
│   │   └── config/                     # 配置文件
│   │       ├── app.config.js           # 应用配置
│   │       └── database.config.js      # 数据库配置
│   └── frontend/                       # 前端容器
│       ├── Dockerfile                  # 前端镜像构建
│       ├── docker-compose.yml          # 前端编排
│       ├── src/                        # 前端源码
│       │   ├── package.json            # 前端依赖
│       │   ├── public/                 # 静态资源
│       │   └── src/                    # 源代码
│       └── config/                     # 配置文件
│           └── nginx.conf              # Nginx配置
│
├── src/                                # 源代码目录
│   ├── README.md                       # 源码说明
│   ├── datasource/                     # 数据源应用
│   │   ├── database/                   # 数据库相关
│   │   │   ├── schema.sql              # 数据库结构
│   │   │   ├── data-generator.py       # 数据生成器
│   │   │   └── migration/              # 数据库迁移
│   │   ├── api/                        # 数据API
│   │   │   ├── app.py                  # Flask应用
│   │   │   ├── routes.py               # 路由定义
│   │   │   └── models.py               # 数据模型
│   │   └── scripts/                    # 数据脚本
│   │       ├── init-database.py        # 数据库初始化
│   │       └── generate-test-data.py   # 测试数据生成
│   ├── resling-app/                    # Resling应用
│   │   ├── backend/                    # 后端代码
│   │   │   ├── app.js                  # 主应用文件
│   │   │   ├── routes/                 # 路由模块
│   │   │   ├── controllers/            # 控制器
│   │   │   ├── models/                 # 数据模型
│   │   │   └── middleware/             # 中间件
│   │   ├── api/                        # API接口
│   │   │   ├── device-control.js       # 设备控制API
│   │   │   ├── data-monitor.js         # 数据监控API
│   │   │   ├── ai-optimization.js      # AI优化API
│   │   │   └── fault-handling.js       # 故障处理API
│   │   ├── services/                   # 业务服务
│   │   │   ├── ai-service.js           # AI服务
│   │   │   ├── device-service.js       # 设备服务
│   │   │   ├── data-service.js         # 数据服务
│   │   │   └── optimization-service.js # 优化服务
│   │   └── utils/                      # 工具类
│   │       ├── database.js             # 数据库工具
│   │       ├── logger.js               # 日志工具
│   │       └── validator.js            # 验证工具
│   └── frontend/                       # 前端应用
│       ├── src/                        # 前端源码
│       │   ├── components/             # 组件
│       │   │   ├── Dashboard/          # 仪表板组件
│       │   │   ├── DeviceControl/      # 设备控制组件
│       │   │   ├── DataMonitor/        # 数据监控组件
│       │   │   └── AIOptimization/     # AI优化组件
│       │   ├── pages/                  # 页面
│       │   │   ├── Home.js             # 首页
│       │   │   ├── Dashboard.js        # 仪表板
│       │   │   ├── Control.js          # 控制页面
│       │   │   └── Monitor.js          # 监控页面
│       │   ├── services/               # 服务
│       │   │   ├── api.js              # API服务
│       │   │   └── websocket.js        # WebSocket服务
│       │   └── utils/                  # 工具
│       │       ├── charts.js           # 图表工具
│       │       └── formatter.js        # 格式化工具
│       ├── public/                     # 静态资源
│       │   ├── index.html              # 主页面
│       │   ├── favicon.ico             # 图标
│       │   └── assets/                 # 资源文件
│       └── package.json                # 前端依赖
│
├── prototype/                          # 原型设计目录
│   ├── ui-mockups/                     # UI原型
│   │   ├── dashboard-mockup.png        # 仪表板原型
│   │   ├── control-mockup.png          # 控制页面原型
│   │   ├── monitor-mockup.png          # 监控页面原型
│   │   └── mobile-mockup.png           # 移动端原型
│   ├── wireframes/                     # 线框图
│   │   ├── dashboard-wireframe.png     # 仪表板线框
│   │   ├── control-wireframe.png       # 控制页面线框
│   │   └── monitor-wireframe.png       # 监控页面线框
│   └── user-flow/                      # 用户流程图
│       ├── main-flow.png               # 主要流程
│       ├── control-flow.png            # 控制流程
│       └── monitor-flow.png            # 监控流程
│
├── design/                             # 设计文档目录
│   ├── architecture/                   # 架构设计
│   │   ├── system-architecture.md      # 系统架构设计
│   │   ├── data-flow.md                # 数据流设计
│   │   ├── api-design.md               # API设计
│   │   └── database-design.md          # 数据库设计
│   ├── ui-design/                      # UI设计
│   │   ├── design-system.md            # 设计系统
│   │   ├── color-palette.md            # 色彩方案
│   │   ├── typography.md               # 字体设计
│   │   └── component-library.md        # 组件库
│   └── system-design/                  # 系统设计
│       ├── business-logic.md           # 业务逻辑设计
│       ├── algorithm-design.md         # 算法设计
│       └── integration-design.md       # 集成设计
│
├── requirements/                       # 需求文档目录
│   ├── README.md                       # 需求说明
│   ├── functional/                     # 功能需求
│   │   ├── functional-requirements.md  # 功能需求规格
│   │   ├── user-stories.md             # 用户故事
│   │   ├── use-cases.md                # 用例分析
│   │   └── feature-modules.md          # 功能模块划分
│   ├── technical/                      # 技术需求
│   │   ├── technical-requirements.md   # 技术需求文档
│   │   ├── architecture-requirements.md # 架构需求
│   │   ├── performance-requirements.md # 性能需求
│   │   ├── security-requirements.md    # 安全需求
│   │   └── compatibility-requirements.md # 兼容性需求
│   └── performance/                    # 性能需求
│       ├── performance-metrics.md      # 性能指标
│       ├── load-testing.md             # 负载测试
│       ├── stress-testing.md           # 压力测试
│       └── optimization-requirements.md # 优化需求
│
├── deployment/                         # 部署目录
│   ├── README.md                       # 部署说明
│   ├── scripts/                        # 部署脚本
│   │   ├── start-demo.sh               # 启动演示脚本
│   │   ├── stop-demo.sh                # 停止演示脚本
│   │   ├── backup-data.sh              # 数据备份脚本
│   │   ├── monitor-system.sh           # 系统监控脚本
│   │   └── maintenance.sh              # 维护脚本
│   ├── config/                         # 配置文件
│   │   ├── environment.env             # 环境变量
│   │   ├── docker-compose.override.yml # Docker覆盖配置
│   │   ├── network-config.yml          # 网络配置
│   │   ├── database-config.yml         # 数据库配置
│   │   └── app-config.yml              # 应用配置
│   └── monitoring/                     # 监控配置
│       ├── prometheus.yml              # Prometheus配置
│       ├── grafana-dashboard.json      # Grafana仪表板
│       ├── alert-rules.yml             # 告警规则
│       ├── log-config.yml              # 日志配置
│       └── health-check.yml            # 健康检查
│
└── assets/                             # 资源文件目录
    ├── images/                         # 图片资源
    │   ├── screenshots/                # 截图
    │   ├── diagrams/                   # 图表
    │   └── icons/                      # 图标
    ├── icons/                          # 图标资源
    │   ├── app-icon.png                # 应用图标
    │   ├── favicon.ico                 # 网站图标
    │   └── ui-icons/                   # UI图标集
    ├── data-samples/                   # 数据样本
    │   ├── historical-data.csv         # 历史数据样本
    │   ├── real-time-data.json         # 实时数据样本
    │   └── test-data.sql               # 测试数据
    └── logos/                          # Logo资源
        ├── hvac-logo.png              # HVAC Logo
        ├── company-logo.png            # 公司Logo
        └── demo-logo.png               # Demo Logo
```

## 文件命名规范

### 文档文件
- 使用英文命名
- 单词间用连字符分隔
- 使用小写字母
- 示例：`functional-requirements.md`

### 代码文件
- 使用驼峰命名法
- 类名使用大驼峰
- 函数名使用小驼峰
- 示例：`deviceControl.js`

### 配置文件
- 使用点分隔
- 使用小写字母
- 示例：`docker-compose.yml`

## 版本控制

### Git忽略文件
- `node_modules/`
- `dist/`
- `build/`
- `*.log`
- `.env`
- `.DS_Store`

### 分支策略
- `main`: 主分支
- `develop`: 开发分支
- `feature/*`: 功能分支
- `hotfix/*`: 热修复分支

## 开发流程

1. **需求分析** → `requirements/`
2. **设计规划** → `design/`
3. **原型设计** → `prototype/`
4. **代码开发** → `src/`
5. **容器化** → `docker/`
6. **部署测试** → `deployment/`
7. **文档编写** → `docs/`

## 注意事项

- 所有文档使用Markdown格式
- 代码需要添加注释
- 配置文件需要版本控制
- 敏感信息不要提交到仓库
- 定期备份重要数据
