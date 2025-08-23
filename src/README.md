# Source Code Directory

# 源代码目录

## Directory Description / 目录说明

**English:**
This directory contains source code for three core applications.

**中文:**
本目录包含三个核心应用的源代码。

## Project Structure / 项目结构

**English:**
```
src/
├── datasource/          # Data source application
│   ├── database/        # Database related
│   ├── api/             # Data API
│   └── scripts/         # Data scripts
├── resling-app/         # Resling application
│   ├── backend/         # Backend code
│   ├── api/             # API interfaces
│   ├── services/        # Business services
│   └── utils/           # Utility classes
└── frontend/            # Frontend application
    ├── src/             # Frontend source code
    ├── public/          # Static resources
    ├── components/      # Components
    └── pages/           # Pages
```

**中文:**
```
src/
├── datasource/          # 数据源应用
│   ├── database/        # 数据库相关
│   ├── api/             # 数据API
│   └── scripts/         # 数据脚本
├── resling-app/         # Resling应用
│   ├── backend/         # 后端代码
│   ├── api/             # API接口
│   ├── services/        # 业务服务
│   └── utils/           # 工具类
└── frontend/            # 前端应用
    ├── src/             # 前端源码
    ├── public/          # 静态资源
    ├── components/      # 组件
    └── pages/           # 页面
```

## Technology Stack / 技术栈

### datasource/ / 数据源
**English:**
- Database: MySQL 8.0
- Language: SQL, Python
- Framework: Flask (API)

**中文:**
- 数据库：MySQL 8.0
- 语言：SQL, Python
- 框架：Flask (API)

### resling-app/ / Resling应用
**English:**
- Backend: Node.js/Python
- Framework: Express/FastAPI
- Database: MySQL
- Message Queue: Redis

**中文:**
- 后端：Node.js/Python
- 框架：Express/FastAPI
- 数据库：MySQL
- 消息队列：Redis

### frontend/ / 前端
**English:**
- Framework: React/Vue.js
- UI Library: Ant Design/Element UI
- Charts: ECharts/D3.js
- Build: Webpack/Vite

**中文:**
- 框架：React/Vue.js
- UI库：Ant Design/Element UI
- 图表：ECharts/D3.js
- 构建：Webpack/Vite

## Development Environment / 开发环境

### Prerequisites / 环境要求
**English:**
- Node.js 16+
- Python 3.8+
- MySQL 8.0+
- Redis 6.0+

**中文:**
- Node.js 16+
- Python 3.8+
- MySQL 8.0+
- Redis 6.0+

### Development Tools / 开发工具
**English:**
- VS Code
- Git
- Docker Desktop

**中文:**
- VS Code
- Git
- Docker Desktop

## Development Process / 开发流程

**English:**
1. Clone the project
2. Install dependencies
3. Configure environment variables
4. Start development server
5. Write code
6. Test and verify
7. Submit code

**中文:**
1. 克隆项目
2. 安装依赖
3. 配置环境变量
4. 启动开发服务器
5. 编写代码
6. 测试验证
7. 提交代码

## Code Standards / 代码规范

**English:**
- Follow ESLint/Prettier standards
- Use TypeScript for type checking
- Write unit tests
- Add comments and explanations
- Follow Git commit standards

**中文:**
- 遵循ESLint/Prettier规范
- 使用TypeScript进行类型检查
- 编写单元测试
- 添加注释说明
- 遵循Git提交规范
