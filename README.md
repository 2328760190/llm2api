# LLM2 API 项目

## 简介

LLM2 API 是一个强大的 AI 聊天接口，为开发者提供了简单易用的方式来集成先进的语言模型功能。本项目封装了复杂的后端逻辑，让您可以专注于应用开发，而无需担心底层实现细节。

## 特性

- 简单易用的 API 接口
- 支持流式和非流式响应
- 内置的负载均衡和错误重试机制
- 灵活的配置选项
- 详细的使用统计和监控

## 快速开始

### 前提条件

- Docker 已安装

### 运行容器

使用以下命令启动 LLM2 API 容器：

```bash
docker run -d --name llm2api \
  -p <host_port>:9999 \
  -v /path/to/host/cookie.txt:/cookie.txt \
  chb2024/llm2api:2.0.0

未完待续...readme没空写
