# Janus-Trader: AI Multi-Agent Investment System

> **Project Codename**: Janus (The Two-Faced God of Beginnings and Endings)
> **Core Objective**: To simulate a professional hedge fund workflow using Multi-Agent collaboration, specifically tailored for the A-Share market with a constrained capital (e.g., ¥100,000 CNY).

## 1. System Architecture

The system operates on a linear **"Waterfall" pipeline**. Each agent consumes the output of the previous agent and appends their own reasoning.

```mermaid
graph TD
    User[User Input] --> Scout[Agent 1: Data Scout]
    Scout --> Analyst[Agent 2: Alpha Hunter]
    Analyst --> Risk[Agent 3: Risk Officer]
    Risk --> Executor[Agent 4: Executor]
    Executor --> CIO[Agent 5: CIO]
    CIO --> Report[Final Investment Decision]