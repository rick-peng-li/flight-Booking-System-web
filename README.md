<!-- 项目 Git 地址: https://github.com/your-username/flight-Booking-System-web -->

# ✈️ Flight Booking System

一个功能完善的机票预订系统，采用前后端分离架构，支持用户注册登录、航班查询、机票预订等功能。

## 🏗️ 项目架构

### 技术栈

| 层级 | 技术 |
|------|------|
| **前端** | React 18 + TypeScript + Redux Toolkit |
| **后端** | Express.js + TypeScript |
| **数据库** | MongoDB + Mongoose |
| **UI组件** | Material-UI (MUI) |
| **认证** | JWT (JSON Web Token) |
| **密码加密** | bcryptjs |

### 项目结构

```
flight-Booking-System-web/
├── client/                    # 前端应用
│   ├── public/               # 静态资源
│   └── src/
│       ├── app/              # Redux store 配置
│       ├── components/       # 公共组件
│       ├── features/         # 功能模块 (登录、注册)
│       └── utils/            # 工具函数
├── config/                   # 配置文件
├── controllers/              # 控制器
├── middleware/               # 中间件
├── models/                   # 数据模型
├── routes/                   # 路由配置
├── services/                 # 业务逻辑
├── utils/                    # 工具函数
└── server.ts                 # 服务入口
```

## 🚀 启动方式

### 前置要求

- Node.js >= 16.6.0
- npm >= 8.11.0
- MongoDB 数据库

### 安装依赖

```bash
# 安装根目录和前端依赖
yarn install
# 或
npm install
```

### 启动开发模式

```bash
# 同时启动前端和后端开发服务器
yarn dev
# 或
npm run dev
```

### 单独启动

```bash
# 启动后端服务 (端口 8000)
yarn server

# 启动前端服务 (端口 3000)
yarn client
```

### 生产环境构建

```bash
# 构建项目
yarn build

# 启动生产服务器
yarn start
```

## 📝 环境配置

在项目根目录创建 `.env` 文件，配置如下：

```env
PORT=8000
MONGO_URI=mongodb://localhost:27017/flight-booking
JWT_SECRET=your-secret-key
```

## ✨ 功能特性

- ✅ 用户注册与登录
- ✅ JWT 身份认证与授权
- ✅ 密码 bcrypt 加密存储
- ✅ 航班信息查询
- ✅ 机票预订
- ✅ 原子性操作防止座位超售（支持并发预订）
- ✅ 响应式前端界面

## 📄 API 路由

| 方法 | 路由 | 描述 |
|------|------|------|
| POST | `/api/auth/register` | 用户注册 |
| POST | `/api/auth/login` | 用户登录 |
| GET | `/api/flights` | 获取航班列表 |
| GET | `/api/flights/:id` | 获取航班详情 |
| POST | `/api/tickets/book` | 预订机票 |
| GET | `/api/tickets/user/:userId` | 获取用户订单 |

## 📄 许可证

ISC License
