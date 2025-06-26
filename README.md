# LearnShareHub 🎓

> 校园学习交流平台 - 让知识分享更简单

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js Version](https://img.shields.io/badge/node-%3E%3D16.0.0-brightgreen)](https://nodejs.org/)
[![React Version](https://img.shields.io/badge/react-18.x-blue)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/typescript-5.x-blue)](https://www.typescriptlang.org/)

## 📖 项目简介

LearnShareHub 是一个专为校园设计的学习交流平台，类似于百度贴吧的模式，但专注于学术交流。学生可以在各个科目板块下分享学习资料、讨论课程内容、交流学习心得。

### ✨ 核心特色

- 🏫 **科目分类**: 按学科组织的讨论板块
- 📚 **资料分享**: 支持多种格式的学习资料上传
- 💬 **实时讨论**: 课程讨论和学习交流
- 👥 **学习小组**: 组建学习小组，协作学习
- 🔍 **智能搜索**: 快速找到相关学习资源
- 📱 **响应式设计**: 支持手机、平板、电脑多端访问

## 🛠️ 技术栈

### 前端
- **框架**: React 18 + TypeScript
- **构建工具**: Vite
- **UI 组件库**: Ant Design 5.x
- **状态管理**: Redux Toolkit + RTK Query
- **路由**: React Router v6
- **样式**: CSS Modules + Less
- **富文本编辑**: React Quill
- **图表**: Recharts

### 后端
- **运行时**: Node.js 18+
- **框架**: Express.js + TypeScript
- **数据库**: PostgreSQL
- **ORM**: Sequelize
- **缓存**: Redis
- **认证**: JWT
- **文件存储**: 本地存储 / 云存储
- **API文档**: Swagger

### 开发工具
- **代码规范**: ESLint + Prettier
- **提交规范**: Conventional Commits
- **容器化**: Docker + Docker Compose
- **CI/CD**: GitHub Actions

## 🚀 快速开始

### 环境要求

- Node.js >= 16.0.0
- npm >= 8.0.0
- PostgreSQL >= 13
- Redis >= 6.0

### 安装依赖

```bash
# 克隆项目
git clone https://github.com/your-username/LearnShareHub.git
cd LearnShareHub

# 安装所有依赖
npm run install:all
```

### 环境配置

1. 复制环境变量文件：
```bash
cp backend/.env.example backend/.env
cp frontend/.env.example frontend/.env
```

2. 配置数据库连接（编辑 `backend/.env`）：
```env
DB_HOST=localhost
DB_PORT=5432
DB_NAME=learnsharehub
DB_USER=your_username
DB_PASSWORD=your_password

REDIS_HOST=localhost
REDIS_PORT=6379

JWT_SECRET=your_jwt_secret
```

### 启动开发服务器

```bash
# 启动前后端开发服务器
npm run dev

# 或者分别启动
npm run dev:frontend  # 前端: http://localhost:5173
npm run dev:backend   # 后端: http://localhost:3000
```

### 数据库初始化

```bash
# 进入后端目录
cd backend

# 运行数据库迁移
npm run db:migrate

# 填充示例数据（可选）
npm run db:seed
```

## 📁 项目结构

```
LearnShareHub/
├── frontend/                 # React 前端应用
│   ├── src/
│   │   ├── components/       # 可复用组件
│   │   ├── pages/           # 页面组件
│   │   ├── store/           # Redux 状态管理
│   │   ├── services/        # API 服务
│   │   ├── hooks/           # 自定义 Hooks
│   │   ├── utils/           # 工具函数
│   │   └── types/           # TypeScript 类型定义
│   ├── public/              # 静态资源
│   ├── package.json
│   └── vite.config.ts
├── backend/                  # Node.js 后端服务
│   ├── src/
│   │   ├── controllers/     # 控制器
│   │   ├── models/          # 数据模型
│   │   ├── routes/          # 路由定义
│   │   ├── middleware/      # 中间件
│   │   ├── services/        # 业务逻辑
│   │   ├── utils/           # 工具函数
│   │   └── types/           # TypeScript 类型定义
│   ├── migrations/          # 数据库迁移文件
│   ├── seeders/             # 数据库种子文件
│   ├── package.json
│   └── tsconfig.json
├── shared/                   # 前后端共享代码
│   ├── types/               # 共享类型定义
│   └── utils/               # 共享工具函数
├── docs/                     # 项目文档
│   ├── api/                 # API 文档
│   └── deployment/          # 部署文档
├── docker-compose.yml        # Docker 编排文件
├── package.json             # 根目录脚本管理
└── README.md
```

## 🔧 开发指南

### 代码规范

我们使用 ESLint 和 Prettier 来保持代码风格一致：

```bash
# 检查代码规范
npm run lint

# 自动修复代码格式
npm run lint:fix
```

### 提交规范

请遵循 [Conventional Commits](https://www.conventionalcommits.org/) 规范：

```
feat: 添加用户注册功能
fix: 修复文件上传bug
docs: 更新API文档
style: 调整登录页面样式
refactor: 重构用户服务模块
test: 添加用户模块单元测试
```

### 分支管理

1. 所有开发必须创建新分支
2. 分支命名规则:
   - `feat/功能名`: 新功能开发
   - `fix/问题描述`: 问题修复
   - `docs/文档更新`: 文档更新
   - `style/样式调整`: 样式调整
3. 禁止直接在 main 分支开发
4. 提交 PR 前请确保通过所有测试

## 🧪 测试

```bash
# 运行前端测试
npm run test:frontend

# 运行后端测试
npm run test:backend

# 运行所有测试
npm run test

# 生成测试覆盖率报告
npm run test:coverage
```

## 📦 构建和部署

### 本地构建

```bash
# 构建前端
npm run build:frontend

# 构建后端
npm run build:backend

# 构建所有
npm run build
```

### Docker 部署

```bash
# 使用 Docker Compose 启动所有服务
docker-compose up -d

# 查看服务状态
docker-compose ps

# 查看日志
docker-compose logs -f
```

### 生产环境部署

详细的部署指南请参考 [部署文档](docs/deployment/README.md)。

## 🤝 贡献指南

我们欢迎所有形式的贡献！请阅读 [贡献指南](CONTRIBUTING.md) 了解如何参与项目开发。

### 如何贡献

1. Fork 本仓库
2. 创建你的特性分支 (`git checkout -b feat/amazing-feature`)
3. 提交你的修改 (`git commit -m 'feat: add amazing feature'`)
4. 推送到分支 (`git push origin feat/amazing-feature`)
5. 打开一个 Pull Request

## 📄 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 🙏 致谢

感谢所有为这个项目做出贡献的开发者！

## 📞 联系我们

- 项目主页: [GitHub Repository](https://github.com/your-username/LearnShareHub)
- 问题反馈: [Issues](https://github.com/your-username/LearnShareHub/issues)
- 讨论交流: [Discussions](https://github.com/your-username/LearnShareHub/discussions)

---

⭐ 如果这个项目对你有帮助，请给我们一个 Star！
