# HVAC Energy Optimizing System Demo Project

# HVAC能源优化系统演示项目

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)](https://github.com/grekyin/hvac-energy-optimizing-demo)
[![Docker](https://img.shields.io/badge/docker-ready-blue.svg)](https://www.docker.com/)

## Project Overview / 项目概述

**English:**
HVAC Energy Optimizing System Demo is an exhibition demonstration system for industrial HVAC energy-saving intelligent control. The system uses Docker containerization deployment and consists of three core components: data source, Resling application, and frontend interface.

**中文:**
HVAC能源优化系统演示是一个用于展览会演示的工业空调节能智能控制系统。系统采用Docker容器化部署，包含三个核心组件：数据源、Resling应用和前端界面。

## Features / 功能特性

**English:**
- 🏭 Real-time industrial HVAC system monitoring
- 🤖 AI-powered intelligent optimization
- 📊 Interactive data visualization
- 🔧 Automated fault detection and recovery
- 🌐 Multi-language support (English/Chinese)
- 🐳 Docker containerized deployment
- 📱 Responsive web interface

**中文:**
- 🏭 实时工业空调系统监控
- 🤖 AI驱动的智能优化
- 📊 交互式数据可视化
- 🔧 自动化故障检测和恢复
- 🌐 多语言支持（英文/中文）
- 🐳 Docker容器化部署
- 📱 响应式Web界面

## System Architecture / 系统架构

### Three Docker Containers / 三个Docker容器

**English:**
1. **Data Source Container (datasource)**
   - Provides historical and real-time data
   - Simulates industrial HVAC system data
   - Port: 3306 (MySQL)

2. **Resling Application Container (resling-app)**
   - Integrates Intouch and Java functionality
   - Provides API services
   - Port: 8080 (API)

3. **Frontend Container (frontend)**
   - Web interface display
   - Real-time data visualization
   - Port: 3000 (Web)

**中文:**
1. **数据源容器 (datasource)**
   - 提供历史数据和实时数据
   - 模拟工业空调系统数据
   - 端口：3306 (MySQL)

2. **Resling应用容器 (resling-app)**
   - 整合Intouch和Java功能
   - 提供API服务
   - 端口：8080 (API)

3. **前端容器 (frontend)**
   - Web界面展示
   - 实时数据可视化
   - 端口：3000 (Web)

## Quick Start / 快速开始

### Prerequisites / 环境要求

**English:**
- Windows 10/11
- Docker Desktop
- Browser (Chrome, Firefox, Edge)

**中文:**
- Windows 10/11
- Docker Desktop
- 浏览器（Chrome、Firefox、Edge）

### Installation / 安装步骤

**English:**
```bash
# Clone the repository
git clone https://github.com/grekyin/hvac-energy-optimizing-demo.git
cd hvac-energy-optimizing-demo

# Start the demo system
docker-compose up -d

# Access the application
# Open browser and navigate to: http://localhost:3000
```

**中文:**
```bash
# 克隆仓库
git clone https://github.com/grekyin/hvac-energy-optimizing-demo.git
cd hvac-energy-optimizing-demo

# 启动演示系统
docker-compose up -d

# 访问应用
# 打开浏览器并访问: http://localhost:3000
```

## Demo Features / 演示功能

**English:**
- Real-time data monitoring
- AI control effect demonstration
- Fault handling demonstration
- Performance metrics display
- Interactive operation functions

**中文:**
- 实时数据监控
- AI控制效果展示
- 故障处理演示
- 性能指标展示
- 交互操作功能

## Documentation / 文档

**English:**
- [API Documentation](docs/en/api/)
- [User Guide](docs/en/user-guide/)
- [Developer Guide](docs/en/developer-guide/)
- [Deployment Guide](docs/en/deployment/)

**中文:**
- [API文档](docs/zh/api/)
- [用户指南](docs/zh/user-guide/)
- [开发者指南](docs/zh/developer-guide/)
- [部署指南](docs/zh/deployment/)

## Contributing / 贡献

**English:**
We welcome contributions from developers worldwide! Please read our [Contributing Guide](CONTRIBUTING.md) and [Code of Conduct](CODE_OF_CONDUCT.md) before submitting your contribution.

**中文:**
我们欢迎全球开发者的贡献！请在提交贡献之前阅读我们的[贡献指南](CONTRIBUTING.md)和[行为准则](CODE_OF_CONDUCT.md)。

## International Collaboration / 国际协作

**English:**
This project supports international collaboration with bilingual documentation and code comments. We encourage contributions from developers around the world.

**中文:**
本项目支持国际协作，提供双语文档和代码注释。我们鼓励全球开发者的贡献。

## License / 许可证

**English:**
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

**中文:**
本项目采用 MIT 许可证 - 详情请参阅 [LICENSE](LICENSE) 文件。

## Contact / 联系方式

**English:**
- Project Issues: [GitHub Issues](https://github.com/grekyin/hvac-energy-optimizing-demo/issues)
- Email: yinguancheng@icloud.com
- Website: https://github.com/grekyin

**中文:**
- 项目问题: [GitHub Issues](https://github.com/grekyin/hvac-energy-optimizing-demo/issues)
- 邮箱: yinguancheng@icloud.com
- 网站: https://github.com/grekyin

## Acknowledgments / 致谢

**English:**
Thanks to all contributors and the open source community for their support and contributions to this project.

**中文:**
感谢所有贡献者和开源社区对本项目的支持和贡献。
