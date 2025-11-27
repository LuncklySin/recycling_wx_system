# ♻️ 废品回收小程序 - 更多在微信 ： jackSinWu --在咸鱼：不知名选手java小鑫

废品回收积分兑换系统是一个集 **环保回收、积分管理、商品兑换、社区互动** 于一体的综合服务平台，旨在推动绿色生活方式，鼓励居民积极参与废品回收，通过积分奖励体系提升用户粘性与社区参与度。


<img width="453" height="965" alt="image" src="https://github.com/user-attachments/assets/7be5fcf1-2ea4-43d5-a22c-70d55c16a8e5" />

<img width="477" height="990" alt="image" src="https://github.com/user-attachments/assets/a6db93ac-3a70-4008-8910-035f7dfbed45" />


<img width="450" height="962" alt="image" src="https://github.com/user-attachments/assets/84d89428-ad52-4893-aa2e-ab0f6e7965ed" />


<img width="487" height="980" alt="image" src="https://github.com/user-attachments/assets/52e7766d-e491-4bd9-8da2-7f553bb7f574" />


<img width="2364" height="1311" alt="e116f466c60f836b99832741325e5938" src="https://github.com/user-attachments/assets/96e77998-8382-4f0f-975c-5c8e9650b915" />


## 🛠 技术栈

- **前端**：Vue.js + Vuex  
- **后端**：Spring Boot + MyBatis + Shiro + Netty  
- **数据库**：MySQL  
- **对象存储**：MinIO

---

## 🌟 核心功能模块

### 4.1 用户管理模块

- 用户注册与登录  
- 个人信息管理  
- 地址信息管理（社区、楼栋、门牌号）  
- 消息通知管理（系统消息、兑换通知、回收提醒）

---

### 4.2 商品管理模块（积分商城）

- 商品分类管理（生活用品、电子产品、环保商品等）  
- 商品信息管理（兑换所需积分、库存、图片等）  
- 商品属性管理（颜色、型号、规格等）  
- 商品评价管理（用户对兑换商品的反馈）  
- 商品库存管理（出库、补货提醒）

---

### 4.3 积分与订单管理模块

- 回收积分记录查询  
- 购物车管理（兑换商品暂存）  
- 创建兑换订单与积分扣除  
- 订单状态跟踪（待发货、已完成等）  
- 订单评价与售后管理

---

### 4.4 社区互动模块

- 发帖分享回收经验与成果  
- 评论、点赞、收藏功能  
- 公告通知（平台活动、兑换活动、新品上架）  
- 用户互动管理（举报机制、内容审核）

---

### 4.6 后台管理模块

- 用户信息与积分管理  
- 商品与兑换管理  
- 订单审核与发货管理  
- 社区内容管理（发帖审核、评论处理）  
- 系统配置管理（积分规则、通知模板等）  
- 权限管理（管理员、社区运营人员等角色权限控制）

---

### 4.7 回收记录与积分生成模块

#### 🧍 用户端功能

- 上传回收订单（上传照片、选择回收类型、重量）  
- 查看回收记录（含审核状态、获得积分）  
- 自动根据回收种类与重量生成积分  
- 积分明细查看（来源、时间、用途）

#### 👨‍💼 管理员端功能

- 审核回收订单（判断有效性、核定积分）  
- 设置回收积分规则（如 1kg 纸类 = 10 分）  
- 调整用户积分  
- 回收统计报表（按时间、类型、用户生成图表）

---

## 🚀 项目部署指南

### ✅ 环境要求

| 环境组件 | 版本要求 |
|----------|----------|
| JDK      | 11 及以上 |
| Node.js  | 16 及以上 |
| MySQL    | 8 及以上 |
| MinIO    | 任意稳定版本 |

---

### ▶ 后端启动步骤

```bash
# 1. 进入后端项目目录
cd backend

# 2. 使用 Maven 构建项目
mvn clean package

# 3. 启动 Spring Boot 应用
java -jar target/recycle-points-system.jar
```

---

### ▶ 前端启动步骤

```bash
# 1. 进入前端项目目录
cd frontend

# 2. 安装依赖
npm install

# 3. 启动前端项目
npm run serve
```

---

### ▶ MinIO 配置说明

```bash
# 启动 MinIO 示例命令
minio server /data --console-address ":9001"
```

- 控制台地址：[http://localhost:9001](http://localhost:9001)
- 在后端配置文件 `application.yml` 中配置：

```yaml
minio:
  endpoint: http://localhost:9000
  accessKey: your-access-key
  secretKey: your-secret-key
  bucketName: recycle-files
```

---

## 📁 项目目录结构

```
recycle-points-platform/
├── backend/        # 后端 Spring Boot 项目
│   ├── src/main/   # Java 源码
│   ├── resources/  # 配置文件
│   ├── pom.xml     # Maven 配置
├── frontend/       # 前端 Vue 项目
│   ├── src/        # 页面与组件
│   ├── public/     # 静态资源
│   ├── package.json# 前端依赖配置
├── docs/           # 项目文档
├── README.md       # 项目说明
```

---

## 🧠 项目亮点

- ♻ 环保理念落地，鼓励居民主动回收废品  
- 🪙 回收积分兑换商品，激励机制清晰透明  
- 🔐 权限分层清晰，支持运营与审核双向流程  
- 📦 商品兑换模块完善，支持评价与库存  
- 📈 后台统计分析全面，辅助社区运营决策


