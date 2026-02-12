# MemeDex — EasyA Hackathon

A full‑stack meme marketplace and social hub with authentication, profiles, chat, discovery, and gamified community features.

## 7. Demo & 媒体素材（必需）

### a) Demo Video 演示视频
- [assets/video.mp4](assets/video.mp4)

### b) UI Screenshots 界面截图
![Screenshot 1](assets/2.png)
![Screenshot 2](assets/3.png)
![Screenshot 3](assets/4.png)
![Screenshot 4](assets/5.png)
![Screenshot 5](assets/6.png)
![Screenshot 6](assets/7.png)
![Screenshot 7](assets/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20260212114251_1200_36.png)

### c) Blockchain Interaction 区块链交互说明
当前版本为完整的前后端原型与功能演示，核心交互发生在 Web 客户端与后端 API 之间（JWT 认证 + MongoDB 数据存储）。本仓库未包含或调用链上合约/钱包连接的实现，因此**没有实际链上交易或合约交互**。如果需要上链，可在现有的「代币/交易」模块基础上接入 EVM（如 MetaMask + RPC + 合约调用），并将关键交易写入链上。

### d) Walkthrough Video with Audio 带音频的讲解视频
- [assets/video.mp4](assets/video.mp4)（同一视频文件，包含演示 + 讲解 + 仓库结构说明）

## Highlights
- Full auth flow with JWT and MongoDB
- Meme creation, discovery, and social interactions
- Profile system, notifications, and chat modules
- Vue 3 + Vite frontend, Node/Express backend

## Tech Stack
- **Frontend:** Vue 3, Vite
- **Backend:** Node.js, Express
- **Database:** MongoDB (local or Atlas)
- **Auth:** JWT

## Monorepo Layout
- [backend/](backend/) — API server
- [frontend/](frontend/) — Web client

## Quick Start

### 1) Backend
```bash
cd backend
npm install
cp .env_example .env
npm run dev
```

Required environment variables in `.env`:
```
JWT_SECRET=your_secret_here
MONGODB_URI=mongodb://localhost:27017/MemeHub
REVIEWER_REGISTER_SECRET=reviewer-secret
```

The API runs at **http://localhost:3000**.

### 2) Frontend
```bash
cd frontend
npm install
npm run dev
```

The app runs at **http://localhost:5173** (default Vite port).

## Core API (Backend)
- `POST /api/register`
- `POST /api/reviewer/register`
- `POST /api/login`
- `POST /api/reset-password`
- `POST /api/upload-avatar`
- `GET /api/avatars/default`
- `POST /api/avatars/select`

## Scripts

**Backend**
- `npm run dev` — start API with hot reload

**Frontend**
- `npm run dev` — start Vite dev server
- `npm run build` — production build

## Notes
- Use MongoDB Atlas by replacing `MONGODB_URI` with your cluster connection string.
- Keep `JWT_SECRET` and `REVIEWER_REGISTER_SECRET` secure in production.

## License
MIT
