# Model Context Protocol (MCP) 开源发布

**日期：** 2024年11月25日  
**类型：** 产品发布 / 开源

## 描述

Anthropic 开源了 Model Context Protocol (MCP)，这是一个连接 AI 模型与外部工具、数据源和能力的标准。基于 JSON-RPC 2.0，MCP 定义了四种资源类型——Tools、Prompts、Resources 和 Sampling——实现丰富、标准化的集成。

MCP 随后被 OpenAI、Google 和其他主要 AI 实验室采用，成为事实上的行业标准。

## 技术细节

- **协议：** 基于 JSON-RPC 2.0
- **资源类型：**
  - **Tools：** 模型可以调用的函数（API、计算）
  - **Prompts：** 可复用的提示模板
  - **Resources：** 数据源（文件、数据库、订阅）
  - **Sampling：** 自定义采样/解码配置

- **架构：** 客户端-服务器模型；MCP 服务器向 MCP 客户端（AI 应用）暴露能力
- **实现：** 开源 SDK、参考实现、文档
- **采用：** OpenAI、Google 等集成了 MCP 支持

## 意义与影响

- **互操作性：** 在整个生态系统中标准化 AI-工具集成
- **生态策略：** MCP 作为标准增加了 Claude 在工具集成工作流中的相关性
- **采用：** 主要实验室的采用验证了协议设计
- **开发者体验：** 简化了使用外部工具构建 AI 应用
- **战略：** 将 Anthropic 定位为 AI 基础设施的生态领导者

---

# English Original

---

# Model Context Protocol (MCP) Open Source Release

**Date:** November 25, 2024  
**Type:** Product Launch / Open Source

## Description

Anthropic open-sourced the Model Context Protocol (MCP), a standard for connecting AI models to external tools, data sources, and capabilities. Built on JSON-RPC 2.0, MCP defined four resource types—Tools, Prompts, Resources, and Sampling—enabling rich, standardized integrations.

MCP was subsequently adopted by OpenAI, Google, and other major AI labs, becoming a de facto industry standard.

## Technical Details

- **Protocol:** JSON-RPC 2.0 based
- **Resource Types:**
  - **Tools:** Functions the model can call (APIs, computations)
  - **Prompts:** Reusable prompt templates
  - **Resources:** Data sources (files, databases, feeds)
  - **Sampling:** Custom sampling/decoding configurations

- **Architecture:** Client-server model; MCP servers expose capabilities to MCP clients (AI applications)
- **Implementation:** Open source SDK, reference implementations, documentation
- **Adoption:** OpenAI, Google, and others integrated MCP support

## Significance & Impact

- **Interoperability:** Standardized AI-tool integration across the ecosystem
- **Ecosystem Play:** MCP as standard increased Claude's relevance in tool-integrated workflows
- **Adoption:** Major lab adoption validated the protocol design
- **Developer Experience:** Simplified building AI applications with external tools
- **Strategic:** Positioned Anthropic as ecosystem leader in AI infrastructure
