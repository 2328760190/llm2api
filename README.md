# LLM2 API 项目

## 简介

LLM2 API 是一个强大的 AI 聊天接口，为开发者提供了简单易用的方式来集成先进的语言模型功能。本项目封装了复杂的后端逻辑，让您可以专注于应用开发，而无需担心底层实现细节。

## 特性

- [x] 简单易用的 API 接口
- [x] 支持流式和非流式响应
- [x] 内置的负载均衡和错误重试机制
- [x] 灵活的配置选项
- [x] 详细的使用统计和监控
- [x] 安全的授权系统
- [x] Cookie 管理和验证
- [x] 定期 Cookie 检查
- [x] 仪表板用于监控服务状态
- [ ] 图片和文件识别（开发中）
- [ ] 联网搜索功能（计划中）

## 已实现功能详情

1. **API 接口**：提供了符合 OpenAI API 标准的接口，支持 chat completions 功能。

2. **流式和非流式响应**：支持实时流式输出和传统的完整响应两种模式，满足不同场景需求。

3. **负载均衡和错误重试**：实现了多 Cookie 轮询机制，自动重试失败请求，提高系统稳定性。

4. **配置选项**：支持通过环境变量配置 API 密钥、授权码、自定义路径等。

5. **使用统计和监控**：内置仪表板展示请求总数、运行时间、延迟等关键指标。

6. **授权系统**：实现了基于授权码的验证机制，定期检查授权有效性。

7. **Cookie 管理**：支持动态添加、验证和失效处理，确保 API 调用的持续可用性。

8. **定期检查**：自动进行 Cookie 和授权码的定期验证，及时发现和处理问题。

9. **监控仪表板**：提供了直观的 Web 界面，实时展示系统状态和性能指标。

## 快速开始

### 前提条件

- Docker 已安装
- 有效的授权码（可在 [auth.464888.xyz](https://auth.464888.xyz) 查询或获取）

### 部署

使用以下命令启动 LLM2 API 容器：

\`\`\`bash
docker run -d --name llm2api \
  -p <host_port>:9999 \
  -e AUTH_CODE=your_auth_code \
  chb2024/llm2api:2.0.0
\`\`\`

将 `<host_port>` 替换为您希望使用的主机端口，`your_auth_code` 替换为您的授权码。

### 环境变量

- `AUTH_CODE`: 授权码（必需）
- `API_KEY`: 用于验证 API 请求的密钥（可选）
- `API_PATH`: 自定义 API 路径前缀（可选）
- `CHECK_INTERVAL`: Cookie 检查间隔（分钟），默认为 0（不进行定期检查）（可选）

## API 端点

### 1. 聊天完成 `/v1/chat/completions`

#### 非流式请求

\`\`\`python
import requests
import json

url = "http://your_server:port/v1/chat/completions"
headers = {
    "Content-Type": "application/json",
    "Authorization": "Bearer your_api_key"
}
data = {
    "model": "meta-llama/Meta-Llama-3.1-70B-Instruct",
    "messages": [
        {"role": "user", "content": "你好，请介绍一下自己。"}
    ]
}

response = requests.post(url, headers=headers, data=json.dumps(data))
print(response.json())
\`\`\`

#### 流式请求

\`\`\`python
import requests
import json

url = "http://your_server:port/v1/c# LLM2 API 项目

## 简介

LLM2 API 是一个强大的 AI 聊天接口，为开发者提供了简单易用的方式来集成先进的语言模型功能。本项目封装了复杂的后端逻辑，让您可以专注于应用开发，而无需担心底层实现细节。

## 特性

- [x] 简单易用的 API 接口
- [x] 支持流式和非流式响应
- [x] 内置的负载均衡和错误重试机制
- [x] 灵活的配置选项
- [x] 详细的使用统计和监控
- [x] 安全的授权系统
- [x] Cookie 管理和验证
- [x] 定期 Cookie 检查
- [x] 仪表板用于监控服务状态
- [ ] 图片和文件识别（开发中）
- [ ] 联网搜索功能（计划中）

## 已实现功能详情

1. **API 接口**：提供了符合 OpenAI API 标准的接口，支持 chat completions 功能。

2. **流式和非流式响应**：支持实时流式输出和传统的完整响应两种模式，满足不同场景需求。

3. **负载均衡和错误重试**：实现了多 Cookie 轮询机制，自动重试失败请求，提高系统稳定性。

4. **配置选项**：支持通过环境变量配置 API 密钥、授权码、自定义路径等。

5. **使用统计和监控**：内置仪表板展示请求总数、运行时间、延迟等关键指标。

6. **授权系统**：实现了基于授权码的验证机制，定期检查授权有效性。

7. **Cookie 管理**：支持动态添加、验证和失效处理，确保 API 调用的持续可用性。

8. **定期检查**：自动进行 Cookie 和授权码的定期验证，及时发现和处理问题。

9. **监控仪表板**：提供了直观的 Web 界面，实时展示系统状态和性能指标。

## 快速开始

### 前提条件

- Docker 已安装
- 有效的授权码（可在 [auth.464888.xyz](https://auth.464888.xyz) 查询或获取）

### 部署

使用以下命令启动 LLM2 API 容器：

\`\`\`bash
docker run -d --name llm2api \
  -p <host_port>:9999 \
  -e AUTH_CODE=your_auth_code \
  chb2024/llm2api:2.0.0
\`\`\`

将 `<host_port>` 替换为您希望使用的主机端口，`your_auth_code` 替换为您的授权码。

### 环境变量

- `AUTH_CODE`: 授权码（必需）
- `API_KEY`: 用于验证 API 请求的密钥（可选）
- `API_PATH`: 自定义 API 路径前缀（可选）
- `CHECK_INTERVAL`: Cookie 检查间隔（分钟），默认为 0（不进行定期检查）（可选）

## API 端点

### 1. 聊天完成 `/v1/chat/completions`

#### 非流式请求

\`\`\`python
import requests
import json

url = "http://your_server:port/v1/chat/completions"
headers = {
    "Content-Type": "application/json",
    "Authorization": "Bearer your_api_key"
}
data = {
    "model": "meta-llama/Meta-Llama-3.1-70B-Instruct",
    "messages": [
        {"role": "user", "content": "你好，请介绍一下自己。"}
    ]
}

response = requests.post(url, headers=headers, data=json.dumps(data))
print(response.json())
\`\`\`

#### 流式请求

\`\`\`python
import requests
import json

url = "http://your_server:port/v1/chat/completions"
headers = {
    "Content-Type": "application/json",
    "Authorization": "Bearer your_api_key"
}
data = {
    "model": "meta-llama/Meta-Llama-3.1-70B-Instruct",
    "messages": [
        {"role": "user", "content": "你好，请介绍一下自己。"}
    ],
    "stream": True
}

response = requests.post(url, headers=headers, data=json.dumps(data), stream=True)
for line in response.iter_lines():
    if line:
        print(json.loads(line.decode('utf-8').split('data: ')[1]))
\`\`\`

请将 `your_server:port` 替换为您的服务器地址和端口，`your_api_key` 替换为您的 API 密钥（如果已设置）。

### 2. 获取可用模型 `/v1/models`

此端点返回可用的语言模型列表。

\`\`\`python
import requests

url = "http://your_server:port/v1/models"
headers = {
    "Authorization": "Bearer your_api_key"
}

response = requests.get(url, headers=headers)
print(response.json())
\`\`\`

### 3. 仪表板 `/`

访问此端点可以查看 LLM2 API 的实时状态仪表板，包括启动时间、总请求数、延迟等信息。

### 4. 获取 Cookies 列表 `/cookies`

此端点返回当前可用的 Cookies 列表。

\`\`\`python
import requests

url = "http://your_server:port/cookies"
headers = {
    "Authorization": "Bearer your_api_key"
}

response = requests.get(url, headers=headers)
print(response.json())
\`\`\`

### 5. 添加 Cookie `/cookie/add`

此端点用于添加新的 Cookie。

\`\`\`python
import requests
import json

url = "http://your_server:port/cookie/add"
headers = {
    "Content-Type": "application/json",
    "Authorization": "Bearer your_api_key"
}
data = {
    "cookie": "your_new_cookie_value"
}

response = requests.post(url, headers=headers, data=json.dumps(data))
print(response.json())
\`\`\`

注意：添加的 Cookie 会经过验证，只有有效的 Cookie 才会被成功添加。

### 6. 添加 Cookie UI `/cookie`

便捷添加cookie，基于端点5

## 获取授权

- 授权码查询和获取：请访问 [auth.464888.xyz](https://auth.464888.xyz)
- 非商业用途：请联系 hello@464888.xyz，可免费获得授权码和必要资源
- 商业或大量使用：请访问我们的 [商业授权商店](#) (即将上线)

## 如何贡献

虽然本项目不开源，但我们欢迎您通过以下方式贡献：

1. 反馈使用体验和建议
2. 报告遇到的问题
3. 分享您基于 LLM2 API 开发的应用
4. 在社交媒体上分享本项目

如果您觉得本项目对您有帮助，欢迎给我们 Star！您的支持是我们持续改进的动力。

## 注意事项

- 请确保妥善保管您的授权码和 API 密钥（如果已设置）。
- 本项目仅提供 Docker 镜像，不公开源代码。
- 如遇到任何问题或需要支持，请联系项目维护者。

## 许可证

本项目采用专有许可证。未经明确授权，不得使用、修改或分发本软件。

## 联系我们

- 技术支持：support@464888.xyz
- 商务合作：business@464888.xyz
- 官方网站：[暂无](https://github.com/2328760190/llm2api)

感谢您使用 LLM2 API！我们期待看到您基于本项目开发的创新应用。


hat/completions"
headers = {
    "Content-Type": "application/json",
    "Authorization": "Bearer your_api_key"
}
data = {
    "model": "meta-llama/Meta-Llama-3.1-70B-Instruct",
    "messages": [
        {"role": "user", "content": "你好，请介绍一下自己。"}
    ],
    "stream": True
}

response = requests.post(url, headers=headers, data=json.dumps(data), stream=True)
for line in response.iter_lines():
    if line:
        print(json.loads(line.decode('utf-8').split('data: ')[1]))
\`\`\`

请将 `your_server:port` 替换为您的服务器地址和端口，`your_api_key` 替换为您的 API 密钥（如果已设置）。

### 2. 获取可用模型 `/v1/models`

此端点返回可用的语言模型列表。

\`\`\`python
import requests

url = "http://your_server:port/v1/models"
headers = {
    "Authorization": "Bearer your_api_key"
}

response = requests.get(url, headers=headers)
print(response.json())
\`\`\`

### 3. 仪表板 `/`

访问此端点可以查看 LLM2 API 的实时状态仪表板，包括启动时间、总请求数、延迟等信息。

### 4. 获取 Cookies 列表 `/cookies`

此端点返回当前可用的 Cookies 列表。

\`\`\`python
import requests

url = "http://your_server:port/cookies"
headers = {
    "Authorization": "Bearer your_api_key"
}

response = requests.get(url, headers=headers)
print(response.json())
\`\`\`

### 5. 添加 Cookie `/cookie/add`

此端点用于添加新的 Cookie。

\`\`\`python
import requests
import json

url = "http://your_server:port/cookie/add"
headers = {
    "Content-Type": "application/json",
    "Authorization": "Bearer your_api_key"
}
data = {
    "cookie": "your_new_cookie_value"
}

response = requests.post(url, headers=headers, data=json.dumps(data))
print(response.json())
\`\`\`

注意：添加的 Cookie 会经过验证，只有有效的 Cookie 才会被成功添加。

### 6. 添加 Cookie UI `/cookie`

便捷添加cookie，基于端点5

## 获取授权

- 授权码查询和获取：请访问 [auth.464888.xyz](https://auth.464888.xyz)
- 非商业用途：请联系 hello@464888.xyz，可免费获得授权码和必要资源
- 商业或大量使用：请访问我们的 [商业授权商店](#) (即将上线)

## 如何贡献

虽然本项目不开源，但我们欢迎您通过以下方式贡献：

1. 反馈使用体验和建议
2. 报告遇到的问题
3. 分享您基于 LLM2 API 开发的应用
4. 在社交媒体上分享本项目

如果您觉得本项目对您有帮助，欢迎给我们 Star！您的支持是我们持续改进的动力。

## 注意事项

- 请确保妥善保管您的授权码和 API 密钥（如果已设置）。
- 本项目仅提供 Docker 镜像，不公开源代码。
- 如遇到任何问题或需要支持，请联系项目维护者。

## 许可证

本项目采用专有许可证。未经明确授权，不得使用、修改或分发本软件。

## 联系我们

- 技术支持：support@464888.xyz
- 商务合作：business@464888.xyz
- 官方网站：[暂无](https://github.com/2328760190/llm2api)

感谢您使用 LLM2 API！我们期待看到您基于本项目开发的创新应用。


