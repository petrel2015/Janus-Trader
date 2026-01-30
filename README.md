# Janus-Trader: AI Multi-Agent Investment System

English | [中文](./README.zh.md)

> **Project Codename**: Janus (The Two-Faced God of Beginnings and Endings)
> **Core Objective**: To simulate a professional hedge fund workflow using Multi-Agent collaboration, specifically tailored for the A-Share market with a constrained capital (e.g., ¥100,000 CNY).

## 2. Usage Instructions

### Workflow
1. **Input**: Place any supplemental data, internal reports, or specific news in the `input/YYYYMMDD/` directory (e.g., `input/20260130/603259.txt`).
2. **Execute**: Command the system to analyze a sector or stock. The **Data Scout** will prioritize your local files before searching the web.
3. **Output**: The final investment decision and multi-agent reasoning will be saved in the `output/` directory as a Markdown report.

### Example
**Request**: *"Analyze the Low-Altitude Economy sector based on the local policy briefing in today's input folder."*

**Process**:
- **Data Scout** reads `input/20260130/603259.txt`.
- Agents collaborate (Scout -> Hunter -> Officer -> Executor -> CIO).
- **Result** is generated at `output/wuxi_apptec_analysis_20260130.md`.

## 3. Project Structure

```mermaid
graph TD
    User[User Input] --> Scout[Agent 1: Data Scout]
    Scout --> Analyst[Agent 2: Alpha Hunter]
    Analyst --> Risk[Agent 3: Risk Officer]
    Risk --> Executor[Agent 4: Executor]
    Executor --> CIO[Agent 5: CIO]
    CIO --> Report[Final Investment Decision]