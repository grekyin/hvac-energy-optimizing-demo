# Docker 容器目录

本目录包含三个核心Docker容器的配置文件和构建脚本。

## 容器架构

```
docker/
├── datasource/          # 数据源容器
│   ├── Dockerfile       # 数据源镜像构建文件
│   ├── docker-compose.yml
│   ├── init.sql         # 数据库初始化脚本
│   └── data/            # 数据文件
├── resling-app/         # Resling应用容器
│   ├── Dockerfile       # Resling应用镜像构建文件
│   ├── docker-compose.yml
│   ├── app/             # 应用代码
│   └── config/          # 配置文件
└── frontend/            # 前端容器
    ├── Dockerfile       # 前端镜像构建文件
    ├── docker-compose.yml
    ├── src/             # 前端源码
    └── public/          # 静态资源
```

## 容器说明

### datasource/
- 基于MySQL镜像
- 包含历史运行数据
- 提供数据API接口
- 端口：3306

### resling-app/
- 基于Node.js/Python镜像
- 整合Intouch和Java功能
- 提供RESTful API
- 端口：8080

### frontend/
- 基于Nginx镜像
- 提供Web界面
- 实时数据展示
- 端口：3000

## 构建和运行

### 构建所有容器
```bash
docker-compose build
```

### 启动所有服务
```bash
docker-compose up -d
```

### 查看日志
```bash
docker-compose logs -f
```

### 停止服务
```bash
docker-compose down
```

## 网络配置

容器间通过Docker网络进行通信：
- 网络名称：hvac-demo-network
- 数据源容器：datasource:3306
- Resling应用容器：resling-app:8080
- 前端容器：frontend:3000
