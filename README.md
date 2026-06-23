# RouteScope Gateway

> Unified AI API Gateway — one API to access 70+ LLMs including GPT, Claude, Gemini, Qwen, DeepSeek, Doubao, GLM, and more.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

---

## 📋 Table of Contents

- [What is RouteScope?](#-what-is-routescope)
- [Quick Start](#-quick-start)
- [Supported Providers](#-supported-providers)
- [Use Cases](#-use-cases)
- [Documentation](#-documentation)
- [Contributing](#-contributing)
- [FAQ](#-faq)
- [License](#-license)
- [Support](#-support)

---

## ✨ What is RouteScope?

[RouteScope Gateway](https://www.routescope.ai/?utm_source=GitHub&campaignid=75afe494d6404c0fa5ee15611507b356&utm_term=GT) is a lightweight, high-performance proxy that gives you a **single, unified interface** to call 70+ LLM providers — OpenAI, Anthropic, Google, DeepSeek, Qwen, Doubao, and more — using a consistent API format.

Stop juggling multiple SDKs, API keys, and billing systems. RouteScope handles the complexity so you can focus on building your product.

**Key benefits:**

- 🔑 **One API key** for all models
- 🚀 **Smart routing** — automatically route requests to the best available model
- 💰 **Cost optimization** — semantic caching reduces unnecessary token consumption and lowers costs
- 🛡️ **Automatic failover** — switch providers instantly if one goes down
- 📊 **Transparent billing** — know exactly what each request costs

---

## 🚀 Quick Start

### 1. Get Your API Key

- Sign in at [RouteScope](https://www.routescope.ai/?utm_source=GitHub&campaignid=75afe494d6404c0fa5ee15611507b356&utm_term=GT)
- Generate your API Key from the Dashboard

### 2. Set Your Endpoint

Use the API base endpoint from your Dashboard:

https://api.routescope.ai/v1

### 3. Make Your First API Call

RouteScope is fully compatible with OpenAI SDKs. Just change the `base_url` and use your RouteScope API key:

```python
import openai

client = openai.OpenAI(
    base_url="https://api.routescope.ai/v1",
    api_key="YOUR_API_KEY"
)

response = client.chat.completions.create(
    model="YOUR_MODEL_ID",
    messages=[{"role": "user", "content": "Hello, world!"}]
)

print(response.choices[0].message.content)
```

---

## 🔧 Supported Providers

| Provider | Models |
| :--- | :--- |
| **OpenAI** | GPT-5, GPT-5 Pro, GPT-5.1, GPT-5.1-Codex, GPT-5.1-Codex-Max |
| **Anthropic** | Claude Fable 5, Claude Opus 4.5/4.6/4.7/4.8, Claude Sonnet 4.5/4.6, Claude Haiku 4.5 |
| **Google** | Gemini 2.5 Flash/Pro/Lite, Gemini 3 Flash Preview, Gemini 3 Pro Image, Gemini 3.1 Flash/Pro |
| **Alibaba Cloud (Qwen)** | Qwen3.6 27B, Qwen3.6 35B A3B, Qwen3.6 Flash, Qwen3.6 Plus, Qwen3.6 Max Preview, Qwen3.7 Max |
| **ByteDance (Doubao)** | Doubao Seed 1.8/2.0 Lite/2.0 Mini/2.0 Pro, Doubao Seed Character, Doubao Seed Code Preview, Seedance 1.0 Pro |
| **DeepSeek** | DeepSeek V4 Flash, DeepSeek V4 Pro |
| **Zhipu AI (GLM)** | GLM-5.1 |
| **More** | Full provider list available in documentation |

> All models are accessible via a **single unified API** — simply change the `model` parameter in your request. No code changes required.

---

## 💡 Use Cases

- **AI Agents** — route planning steps to Claude, execution to GPT
- **Multi-provider fallback** — automatically switch if one provider fails or rate-limits
- **Cost optimization** — cache repeated prompts to reduce token usage by 30-50%
- **Global teams** — one API key for all projects, track cost per team
- **A/B testing** — compare model outputs by routing percentage of traffic

---

## 📚 Documentation

Full documentation is available at: [https://doc.routescope.ai/](https://doc.routescope.ai/?utm_source=GitHub&campaignid=cc05ee263eb34df0ad970ac7f8356f57&utm_term=GT)

---

## 🤝 Contributing

We welcome contributions!

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request
For details, see [CONTRIBUTING.md](CONTRIBUTING.md) or open an [issue](https://github.com/routescope/gateway/issues).

---

## ❓ FAQ

### Do credits expire? Can I get a refund?

Credits never expire — your top-up credits remain in your account indefinitely. For refunds: unused credits purchased within the last 30 days are fully refundable, no questions asked. Just email us at billing@routescope.ai.


### How does pricing compare to going directly to OpenAI / Anthropic?

For direct model calls, Routescope charges provider cost + $0 (we pass through at cost). In practice, smart routing typically saves 20–40% on your actual spend by selecting the cheapest model that meets your quality threshold. You can see a live pricing breakdown per model in your dashboard before you commit.


### Is it really OpenAI SDK compatible? What do I need to change?

One line: change `base_url` to `https://api.routescope.ai/v1` and swap your key. The OpenAI Python, Node.js, and REST clients all work without any other modification.
Streaming, function calling, vision, embeddings, and audio are fully supported.

---

## 📄 License

MIT © [RouteScope](https://www.routescope.ai/?utm_source=GitHub&campaignid=75afe494d6404c0fa5ee15611507b356&utm_term=GT)

---

## 🌟 Support

- 💬 **Telegram**: [@RouteScopeAPI](https://t.me/RouteScopeAPI)
- 📧 **Email**: [support@routescope.ai](mailto:support@routescope.ai)
- 🐦 **Twitter/X**: [@RouteScopeHQ](https://x.com/RouteScopeHQ)
- 📘 **Facebook**: [RouteScopeHQ](https://www.facebook.com/RouteScopeHQ)
- 💬 **WhatsApp Channel**: [RouteScope](https://whatsapp.com/channel/0029VbCScNTFcowFoyyucO2I)
- ⭐ **Star us on GitHub** — if this project helps you, please give it a star!

---

**Built for developers who want to ship AI products faster.**
