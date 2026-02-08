---
title: "Inkwest"
features:
  - icon: "users"
    title: "Enterprise Ready"
    description: "OIDC authentication, role-based access, session management, and usage budget controls. Single-user dev mode included for quick local setup."
  - icon: "shield"
    title: "Read-Only by Default"
    description: "The AI is instructed to use read-only kubectl commands. Combined with RBAC, you stay in control of what runs on your cluster."
  - icon: "layers"
    title: "Multi-Provider AI"
    description: "Use Anthropic Claude (direct, Bedrock, Azure), OpenRouter, OpenAI, or Google Gemini as your AI backend."
  - icon: "terminal"
    title: "AI Chat Interface"
    description: "Natural language debugging — ask questions about your cluster and get intelligent, context-aware answers."
  - icon: "server"
    title: "Multi-Cluster"
    description: "Connect and switch between multiple Kubernetes clusters with per-cluster access controls."
  - icon: "zap"
    title: "Real-Time Streaming"
    description: "WebSocket-based streaming responses with live tool execution feedback and cancellation support."
steps:
  - number: 1
    title: "Connect"
    description: "Point Inkwest at your Kubernetes clusters via kubeconfig. Set up your preferred AI provider."
  - number: 2
    title: "Ask"
    description: "Describe your issue in natural language — pod crashes, networking problems, resource constraints."
  - number: 3
    title: "Get Answers"
    description: "The AI executes kubectl commands, analyzes output, and walks you through the root cause and fix."
providers:
  - name: "Anthropic Claude"
    note: "Direct API"
    tested: false
  - name: "AWS Bedrock"
    note: "Claude via AWS"
    tested: false
  - name: "Azure AI"
    note: "Claude via Azure"
    tested: false
  - name: "OpenRouter"
    note: "Multi-model gateway"
    tested: true
  - name: "OpenAI"
    note: "GPT models"
    tested: true
  - name: "Google Gemini"
    note: "Gemini models"
    tested: false
  - name: "Anthropic CLI"
    note: "Claude Code"
    tested: true
comparisons:
  - name: "K8sGPT"
    tag: "CNCF Sandbox"
    description: "CLI-based diagnostic scanner with operator mode for continuous monitoring."
    pros:
      - "CNCF-backed, vendor-neutral"
      - "10+ AI backends including local models"
      - "Operator mode for unattended scanning"
    cons:
      - "No web UI or interactive chat"
      - "No multi-user auth or OIDC"
      - "No conversation history"
  - name: "kubectl-ai"
    tag: "Google"
    description: "CLI plugin that translates natural language to kubectl commands."
    pros:
      - "Google-backed, active development"
      - "Natural language to kubectl"
      - "MCP server mode"
    cons:
      - "Single-user CLI tool"
      - "No session persistence"
      - "No multi-cluster management"
  - name: "Komodor"
    tag: "Commercial"
    description: "Enterprise SaaS platform with AI agents for autonomous Kubernetes operations."
    pros:
      - "Most mature commercial AI SRE platform"
      - "Autonomous self-healing"
      - "SOC 2, GDPR, HIPAA compliant"
    cons:
      - "Starts at $1,000/month"
      - "SaaS-only, no self-hosted option"
      - "Single AI provider (Claude/Bedrock)"
  - name: "HolmesGPT"
    tag: "CNCF Sandbox"
    description: "Alert-driven AI investigation engine, powers Microsoft's AKS CLI Agent."
    pros:
      - "Deep Prometheus/alerting integration"
      - "Validated by Microsoft adoption"
      - "Agentic investigation loop"
    cons:
      - "Alert-driven, not user-driven"
      - "Requires existing Prometheus stack"
      - "No standalone web UI"
  - name: "Headlamp"
    tag: "K8s SIG-UI"
    description: "Kubernetes dashboard with an AI assistant plugin (alpha)."
    pros:
      - "Official Kubernetes SIG project"
      - "Full dashboard with AI bolt-on"
      - "Context-aware AI assistant"
    cons:
      - "AI plugin is alpha"
      - "No conversation persistence"
      - "User-managed API keys (not centralized)"
  - name: "Lens Prism"
    tag: "$25/user/mo"
    description: "Desktop IDE with embedded AI copilot for Kubernetes."
    pros:
      - "Polished desktop UX"
      - "Air-gapped environment support"
      - "RBAC-aligned"
    cons:
      - "Desktop only, no web access"
      - "Per-seat commercial licensing"
      - "No multi-user or shared sessions"
---
