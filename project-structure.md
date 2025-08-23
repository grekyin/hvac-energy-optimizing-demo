# HVAC Energy Optimizing System Demo - Complete Project Structure

# HVAC能源优化系统演示项目完整结构说明

## Project Overview / 项目概述

**English:**
HVAC Energy Optimizing System Demo is an exhibition demonstration system for industrial HVAC energy-saving intelligent control. The system uses Docker containerization deployment and consists of three core components.

**中文:**
HVAC能源优化系统演示项目是一个用于展览会演示的工业空调节能智能控制系统，采用Docker容器化部署，包含三个核心组件。

## Complete Directory Structure / 完整目录结构

**English:**
```
hvac-energy-optimizing-demo/
├── README.md                           # Main project documentation
├── project-structure.md                # Project structure documentation
├── CONTRIBUTING.md                     # Contribution guidelines
├── CODE_OF_CONDUCT.md                  # Code of conduct
├── LICENSE                             # MIT License
├── .gitignore                          # Git ignore rules
│
├── docs/                               # Documentation directory
│   ├── README.md                       # Documentation guide
│   ├── en/                             # English documentation
│   │   └── README.md                   # English documentation overview
│   ├── zh/                             # Chinese documentation
│   │   └── README.md                   # Chinese documentation overview
│   ├── api/                            # API documentation
│   │   ├── datasource-api.md           # Data source API documentation
│   │   ├── resling-api.md              # Resling application API documentation
│   │   └── frontend-api.md             # Frontend API documentation
│   ├── user-guide/                     # User guide
│   │   ├── demo-operation-guide.md     # Demo operation guide
│   │   ├── user-manual.md              # User manual
│   │   └── faq.md                      # Frequently asked questions
│   └── developer-guide/                # Developer guide
│       ├── development-setup.md        # Development environment setup
│       ├── coding-standards.md         # Coding standards
│       ├── development-workflow.md     # Development workflow
│       └── testing-guide.md            # Testing guide
│
├── docker/                             # Docker containers directory
│   ├── README.md                       # Docker documentation
│   ├── docker-compose.yml              # Main orchestration file
│   ├── datasource/                     # Data source container
│   │   ├── Dockerfile                  # Data source image build
│   │   ├── docker-compose.yml          # Data source orchestration
│   │   ├── init.sql                    # Database initialization
│   │   ├── data/                       # Data files
│   │   │   ├── historical-data.sql     # Historical data
│   │   │   └── real-time-data.sql      # Real-time data
│   │   └── config/                     # Configuration files
│   │       └── my.cnf                  # MySQL configuration
│   ├── resling-app/                    # Resling application container
│   │   ├── Dockerfile                  # Resling app image build
│   │   ├── docker-compose.yml          # Resling app orchestration
│   │   ├── app/                        # Application code
│   │   │   ├── package.json            # Node.js dependencies
│   │   │   ├── requirements.txt        # Python dependencies
│   │   │   └── src/                    # Source code
│   │   └── config/                     # Configuration files
│   │       ├── app.config.js           # Application configuration
│   │       └── database.config.js      # Database configuration
│   └── frontend/                       # Frontend container
│       ├── Dockerfile                  # Frontend image build
│       ├── docker-compose.yml          # Frontend orchestration
│       ├── src/                        # Frontend source code
│       │   ├── package.json            # Frontend dependencies
│       │   ├── public/                 # Static resources
│       │   └── src/                    # Source code
│       └── config/                     # Configuration files
│           └── nginx.conf              # Nginx configuration
│
├── src/                                # Source code directory
│   ├── README.md                       # Source code documentation
│   ├── datasource/                     # Data source application
│   │   ├── database/                   # Database related
│   │   │   ├── schema.sql              # Database schema
│   │   │   ├── data-generator.py       # Data generator
│   │   │   └── migration/              # Database migrations
│   │   ├── api/                        # Data API
│   │   │   ├── app.py                  # Flask application
│   │   │   ├── routes.py               # Route definitions
│   │   │   └── models.py               # Data models
│   │   └── scripts/                    # Data scripts
│   │       ├── init-database.py        # Database initialization
│   │       └── generate-test-data.py   # Test data generation
│   ├── resling-app/                    # Resling application
│   │   ├── backend/                    # Backend code
│   │   │   ├── app.js                  # Main application file
│   │   │   ├── routes/                 # Route modules
│   │   │   ├── controllers/            # Controllers
│   │   │   ├── models/                 # Data models
│   │   │   └── middleware/             # Middleware
│   │   ├── api/                        # API interfaces
│   │   │   ├── device-control.js       # Device control API
│   │   │   ├── data-monitor.js         # Data monitoring API
│   │   │   ├── ai-optimization.js      # AI optimization API
│   │   │   └── fault-handling.js       # Fault handling API
│   │   ├── services/                   # Business services
│   │   │   ├── ai-service.js           # AI service
│   │   │   ├── device-service.js       # Device service
│   │   │   ├── data-service.js         # Data service
│   │   │   └── optimization-service.js # Optimization service
│   │   └── utils/                      # Utility classes
│   │       ├── database.js             # Database utilities
│   │       ├── logger.js               # Logging utilities
│   │       └── validator.js            # Validation utilities
│   └── frontend/                       # Frontend application
│       ├── src/                        # Frontend source code
│       │   ├── components/             # Components
│       │   │   ├── Dashboard/          # Dashboard component
│       │   │   ├── DeviceControl/      # Device control component
│       │   │   ├── DataMonitor/        # Data monitoring component
│       │   │   └── AIOptimization/     # AI optimization component
│       │   ├── pages/                  # Pages
│       │   │   ├── Home.js             # Home page
│       │   │   ├── Dashboard.js        # Dashboard page
│       │   │   ├── Control.js          # Control page
│       │   │   └── Monitor.js          # Monitor page
│       │   ├── services/               # Services
│       │   │   ├── api.js              # API service
│       │   │   └── websocket.js        # WebSocket service
│       │   └── utils/                  # Utilities
│       │       ├── charts.js           # Chart utilities
│       │       └── formatter.js        # Formatting utilities
│       ├── public/                     # Static resources
│       │   ├── index.html              # Main page
│       │   ├── favicon.ico             # Icon
│       │   └── assets/                 # Asset files
│       └── package.json                # Frontend dependencies
│
├── prototype/                          # Prototype design directory
│   ├── ui-mockups/                     # UI mockups
│   │   ├── dashboard-mockup.png        # Dashboard mockup
│   │   ├── control-mockup.png          # Control page mockup
│   │   ├── monitor-mockup.png          # Monitor page mockup
│   │   └── mobile-mockup.png           # Mobile mockup
│   ├── wireframes/                     # Wireframes
│   │   ├── dashboard-wireframe.png     # Dashboard wireframe
│   │   ├── control-wireframe.png       # Control page wireframe
│   │   └── monitor-wireframe.png       # Monitor page wireframe
│   └── user-flow/                      # User flow diagrams
│       ├── main-flow.png               # Main flow
│       ├── control-flow.png            # Control flow
│       └── monitor-flow.png            # Monitor flow
│
├── design/                             # Design documentation directory
│   ├── architecture/                   # Architecture design
│   │   ├── system-architecture.md      # System architecture design
│   │   ├── data-flow.md                # Data flow design
│   │   ├── api-design.md               # API design
│   │   └── database-design.md          # Database design
│   ├── ui-design/                      # UI design
│   │   ├── design-system.md            # Design system
│   │   ├── color-palette.md            # Color palette
│   │   ├── typography.md               # Typography design
│   │   └── component-library.md        # Component library
│   └── system-design/                  # System design
│       ├── business-logic.md           # Business logic design
│       ├── algorithm-design.md         # Algorithm design
│       └── integration-design.md       # Integration design
│
├── requirements/                       # Requirements documentation directory
│   ├── README.md                       # Requirements documentation
│   ├── functional/                     # Functional requirements
│   │   ├── functional-requirements.md  # Functional requirements specification
│   │   ├── user-stories.md             # User stories
│   │   ├── use-cases.md                # Use case analysis
│   │   └── feature-modules.md          # Feature module division
│   ├── technical/                      # Technical requirements
│   │   ├── technical-requirements.md   # Technical requirements documentation
│   │   ├── architecture-requirements.md # Architecture requirements
│   │   ├── performance-requirements.md # Performance requirements
│   │   ├── security-requirements.md    # Security requirements
│   │   └── compatibility-requirements.md # Compatibility requirements
│   └── performance/                    # Performance requirements
│       ├── performance-metrics.md      # Performance metrics
│       ├── load-testing.md             # Load testing
│       ├── stress-testing.md           # Stress testing
│       └── optimization-requirements.md # Optimization requirements
│
├── deployment/                         # Deployment directory
│   ├── README.md                       # Deployment documentation
│   ├── production/                     # Production deployment
│   │   ├── docker-compose.prod.yml     # Production orchestration
│   │   ├── nginx.conf                  # Nginx configuration
│   │   └── ssl/                        # SSL certificates
│   ├── staging/                        # Staging deployment
│   │   ├── docker-compose.staging.yml  # Staging orchestration
│   │   └── config/                     # Staging configuration
│   └── development/                    # Development deployment
│       ├── docker-compose.dev.yml      # Development orchestration
│       └── config/                     # Development configuration
│
├── assets/                             # Assets directory
│   ├── images/                         # Images
│   │   ├── logo.png                    # Project logo
│   │   ├── screenshots/                # Screenshots
│   │   └── icons/                      # Icons
│   ├── videos/                         # Videos
│   │   └── demo-video.mp4              # Demo video
│   └── documents/                      # Documents
│       ├── presentations/              # Presentations
│       └── reports/                    # Reports
│
└── .github/                            # GitHub configuration
    ├── ISSUE_TEMPLATE/                 # Issue templates
    │   ├── bug_report.md               # Bug report template
    │   └── feature_request.md          # Feature request template
    ├── PULL_REQUEST_TEMPLATE.md        # Pull request template
    └── workflows/                      # GitHub Actions workflows
        └── ci.yml.disabled             # CI workflow (disabled)
```

**中文:**
```
hvac-energy-optimizing-demo/
├── README.md                           # 项目主说明文档
├── project-structure.md                # 项目结构说明文档
├── CONTRIBUTING.md                     # 贡献指南
├── CODE_OF_CONDUCT.md                  # 行为准则
├── LICENSE                             # MIT许可证
├── .gitignore                          # Git忽略规则
│
├── docs/                               # 文档目录
│   ├── README.md                       # 文档说明
│   ├── en/                             # 英文文档
│   │   └── README.md                   # 英文文档概览
│   ├── zh/                             # 中文文档
│   │   └── README.md                   # 中文文档概览
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
│   ├── production/                     # 生产环境部署
│   │   ├── docker-compose.prod.yml     # 生产环境编排
│   │   ├── nginx.conf                  # Nginx配置
│   │   └── ssl/                        # SSL证书
│   ├── staging/                        # 测试环境部署
│   │   ├── docker-compose.staging.yml  # 测试环境编排
│   │   └── config/                     # 测试环境配置
│   └── development/                    # 开发环境部署
│       ├── docker-compose.dev.yml      # 开发环境编排
│       └── config/                     # 开发环境配置
│
├── assets/                             # 资源目录
│   ├── images/                         # 图片
│   │   ├── logo.png                    # 项目logo
│   │   ├── screenshots/                # 截图
│   │   └── icons/                      # 图标
│   ├── videos/                         # 视频
│   │   └── demo-video.mp4              # 演示视频
│   └── documents/                      # 文档
│       ├── presentations/              # 演示文稿
│       └── reports/                    # 报告
│
└── .github/                            # GitHub配置
    ├── ISSUE_TEMPLATE/                 # Issue模板
    │   ├── bug_report.md               # Bug报告模板
    │   └── feature_request.md          # 功能请求模板
    ├── PULL_REQUEST_TEMPLATE.md        # Pull Request模板
    └── workflows/                      # GitHub Actions工作流
        └── ci.yml.disabled             # CI工作流（已禁用）
```
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

## File Naming Conventions / 文件命名规范

### Documentation Files / 文档文件
**English:**
- Use English naming
- Separate words with hyphens
- Use lowercase letters
- Example: `functional-requirements.md`

**中文:**
- 使用英文命名
- 单词间用连字符分隔
- 使用小写字母
- 示例：`functional-requirements.md`

### Code Files / 代码文件
**English:**
- Use camelCase naming
- Class names use PascalCase
- Function names use camelCase
- Example: `deviceControl.js`

**中文:**
- 使用驼峰命名法
- 类名使用大驼峰
- 函数名使用小驼峰
- 示例：`deviceControl.js`

### Configuration Files / 配置文件
**English:**
- Use dot separation
- Use lowercase letters
- Example: `docker-compose.yml`

**中文:**
- 使用点分隔
- 使用小写字母
- 示例：`docker-compose.yml`

## Version Control / 版本控制

### Git Ignore Files / Git忽略文件
**English:**
- `node_modules/`
- `dist/`
- `build/`
- `*.log`
- `.env`
- `.DS_Store`

**中文:**
- `node_modules/`
- `dist/`
- `build/`
- `*.log`
- `.env`
- `.DS_Store`

### Branch Strategy / 分支策略
**English:**
- `main`: Main branch
- `develop`: Development branch
- `feature/*`: Feature branch
- `hotfix/*`: Hotfix branch

**中文:**
- `main`: 主分支
- `develop`: 开发分支
- `feature/*`: 功能分支
- `hotfix/*`: 热修复分支

## Development Process / 开发流程

**English:**
1. **Requirement Analysis** → `requirements/`
2. **Design Planning** → `design/`
3. **Prototype Design** → `prototype/`
4. **Code Development** → `src/`
5. **Containerization** → `docker/`
6. **Deployment Testing** → `deployment/`
7. **Documentation** → `docs/`

**中文:**
1. **需求分析** → `requirements/`
2. **设计规划** → `design/`
3. **原型设计** → `prototype/`
4. **代码开发** → `src/`
5. **容器化** → `docker/`
6. **部署测试** → `deployment/`
7. **文档编写** → `docs/`

## Important Notes / 注意事项

**English:**
- All documents use Markdown format
- Code needs comments
- Configuration files need version control
- Sensitive information should not be committed to repository
- Regularly backup important data

**中文:**
- 所有文档使用Markdown格式
- 代码需要添加注释
- 配置文件需要版本控制
- 敏感信息不要提交到仓库
- 定期备份重要数据
