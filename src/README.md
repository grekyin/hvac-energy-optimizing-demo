# 源代码目录

本目录包含三个核心应用的源代码。

## 项目结构

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

## 技术栈

### datasource/
- 数据库：MySQL 8.0
- 语言：SQL, Python
- 框架：Flask (API)

### resling-app/
- 后端：Node.js/Python
- 框架：Express/FastAPI
- 数据库：MySQL
- 消息队列：Redis

### frontend/
- 框架：React/Vue.js
- UI库：Ant Design/Element UI
- 图表：ECharts/D3.js
- 构建：Webpack/Vite

## 开发环境

### 环境要求
- Node.js 16+
- Python 3.8+
- MySQL 8.0+
- Redis 6.0+

### 开发工具
- VS Code
- Git
- Docker Desktop

## 开发流程

1. 克隆项目
2. 安装依赖
3. 配置环境变量
4. 启动开发服务器
5. 编写代码
6. 测试验证
7. 提交代码

## 代码规范

- 遵循ESLint/Prettier规范
- 使用TypeScript进行类型检查
- 编写单元测试
- 添加注释说明
- 遵循Git提交规范
