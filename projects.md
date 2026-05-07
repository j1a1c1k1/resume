# RAG 智能文档处理系统

> 智能文档处理与检索系统 - 基于检索增强生成(RAG)技术的企业级文档处理平台

## 系统架构

```
文档上传 → OCR识别 → RAG处理 → AI问答 → 结果输出
  ↓          ↓          ↓         ↓         ↓
 PDF/图片  Tesseract  向量检索   大模型    Web展示
```

## 功能模块

### 1. RAG项目 `RAG_project/`
核心RAG检索增强生成模块，支持向量化检索与知识库问答

### 2. 专利处理 `Patent/`
专利文档智能处理系统，支持专利解析、OCR识别与结构化提取

### 3. 模型管理 `models/`
AI模型配置与下载管理，支持多种Embedding模型

### 4. 向量数据库 `chroma_db/`
Chroma向量数据库存储，支持语义检索与相似度匹配

### 5. 知识库 `my_knowledge/`
个人知识库管理，支持文档上传、分类与检索

### 6. 部署配置 `deploy/`
Docker容器化部署配置与Gunicorn服务器部署文档

---

## 核心文件

| 文件 | 说明 |
|-----|------|
| `app.py` | Flask主应用入口，路由配置与API接口定义 |
| `ai_utils.py` | AI工具函数，大模型调用与响应处理 |
| `rag_utils.py` | RAG工具函数，向量检索与知识库查询 |
| `ocr_utils.py` | OCR识别工具，Tesseract集成与文本提取 |
| `db_utils.py` | 数据库工具，SQLite操作与数据持久化 |
| `wsgi.py` | WSGI入口，用于生产环境部署 |
| `Dockerfile` | Docker容器构建配置 |
| `requirements.txt` | Python依赖包清单 |

---

## 技术栈

<div style="display:flex;gap:8px;flex-wrap:wrap;">
<img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white" alt="Python"/>
<img src="https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white" alt="Flask"/>
<img src="https://img.shields.io/badge/LangChain-412991?style=flat&logo=langchain&logoColor=white" alt="LangChain"/>
<img src="https://img.shields.io/badge/ChromaDB-000000?style=flat&logo=chromadb" alt="ChromaDB"/>
<img src="https://img.shields.io/badge/OCR-Tesseract-0057A8?style=flat" alt="OCR"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white" alt="Docker"/>
</div>

---

## 数据目录

| 目录 | 路径 | 说明 |
|-----|------|------|
| 📁 输入文件 | `input/` | 7 PDF + 6 图片 |
| 📁 上传文件 | `uploads/` | 27 PDF + 21 图片 |
| 📁 输出文件 | `outputs/` | 处理结果输出 |
| 📁 Web模拟 | `outputs_web_sim/` | Web界面模拟输出 |
| 📁 调试输出 | `outputs_debug/` | 调试日志与数据 |
| 📁 对比输出 | `outputs_comparison/` | 结果对比分析 |
| 📁 静态资源 | `static/` | CSS/JS/图片 |
| 📁 模板文件 | `templates/` | Jinja2模板 |

---

## 快速开始

```bash
# 克隆项目
git clone https://github.com/j1a1c1k1/RAG-Document-System.git
cd RAG-Document-System

# 安装依赖
pip install -r requirements.txt

# 下载模型
python download_model.py

# 启动服务
python app.py

# 或使用Docker
docker build -t rag-system .
docker run -p 5000:5000 rag-system
```

---

## 项目特色

- 🔍 **智能OCR识别** - 集成PaddleOCR/Tesseract，支持多种文档格式
- 🧠 **向量语义检索** - 基于ChromaDB的高效向量存储与检索
- 💬 **多模型支持** - 支持多种大模型接入，灵活切换
- 🐳 **容器化部署** - 提供Dockerfile，快速部署上线
- 📊 **结果可视化** - 友好的Web界面展示处理结果

---

<p align="center">
  <a href="https://github.com/j1a1c1k1/guojiahao-github-profile">
    ← 返回主页
  </a>
</p>

<p align="center" style="color:#888;font-size:12px;">
  © 2024 Guo Jiahao - RAG Document System
</p>
