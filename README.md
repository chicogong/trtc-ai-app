# TRTC AI App

[![Node.js](https://img.shields.io/badge/Node.js-18+-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-5.x-000000?logo=express&logoColor=white)](https://expressjs.com/)
[![Tencent Cloud](https://img.shields.io/badge/Tencent%20Cloud-TRTC-0052CC?logo=tencentqq&logoColor=white)](https://cloud.tencent.com/product/trtc)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/chicogong/trtc-ai-app?style=social)](https://github.com/chicogong/trtc-ai-app)

基于腾讯云 TRTC 的 AI 实时语音对话应用，集成 ASR（语音识别）、LLM（大语言模型）和 TTS（语音合成）能力。

## 功能特性

- 实时语音对话：基于 TRTC 实现低延迟音视频通信
- 智能语音识别：支持中文 8k 大模型，带降噪功能
- LLM 对话：支持 OpenAI 协议的大语言模型（如 DeepSeek）
- 语音合成：支持多种 TTS 服务商（如 MiniMax）
- 智能打断：支持声纹识别的自动打断模式
- 语义断句：基于语义的智能句子分割

## 快速开始

### 安装依赖

```bash
npm install
```

### 配置

编辑 `server.js` 中的 `CONFIG` 对象，填入以下必要配置：

1. **apiConfig**: 腾讯云 API 密钥
   - `SecretId`: 腾讯云 SecretId
   - `SecretKey`: 腾讯云 SecretKey

2. **trtcConfig**: TRTC 应用配置
   - `sdkAppId`: TRTC 应用 ID
   - `secretKey`: TRTC 密钥

3. **LLMConfig**: 大语言模型配置
   - `Model`: 模型名称
   - `APIUrl`: API 地址
   - `APIKey`: API 密钥

4. **TTSConfig**: 语音合成配置
   - `AppId`: TTS 应用 ID
   - `APIKey`: TTS API 密钥

### 启动服务

```bash
npm start
```

服务默认运行在 `http://127.0.0.1:3000/`

## API 接口

| 接口 | 方法 | 说明 |
|------|------|------|
| `/` | GET | 对话页面 |
| `/getInfo` | POST | 获取用户凭证 |
| `/startConversation` | POST | 启动 AI 对话 |
| `/stopConversation` | POST | 停止 AI 对话 |

## 技术栈

- Node.js + Express
- 腾讯云 TRTC SDK
- TLS Sig API v2

## 相关链接

- [腾讯云 TRTC 文档](https://cloud.tencent.com/document/product/647)
- [TRTC AI 对话文档](https://cloud.tencent.com/document/product/647/108407)

## License

MIT
