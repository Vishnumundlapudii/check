
# AI-Powered Project Management Assistant (Multi-Agent Framework on Azure)

## 🟦 1. Input Sources
- SharePoint  
- MS Teams  
- Databases  
- Text Files  
- Websites  

## 🔄 2. Preprocessing Agent
- Ingests and cleans data from all input sources  
- Normalizes formats and prepares for downstream agents

## 🧭 3. Planner Agent
- Determines which agent(s) to activate based on user request  
- Interfaces with Vector DB / Knowledge Base for historical context  

## 🧠 4. Specialized Task Agents
- **Charter Agent**: Generates detailed Project Charter documents  
- **Status Report Agent**: Builds weekly/monthly progress updates  
- **Financial Overview Agent**: Tracks budgets and cost insights  
- **Milestone Breakdown Agent**: Breaks project phases into manageable chunks  
- **Risk Log Agent**: Monitors project risks and mitigation strategies  
- **Presentation Generator Agent**: Generates stakeholder-ready decks  
- **Stakeholder Communication Agent**: Summarizes updates for stakeholders  
- **Planning & Timeline Agent**: Lays out schedules and dependencies  

## 📊 5. Output Interface
- **Streamlit / Web Dashboard**
  - Upload or connect data sources  
  - Trigger document/report generation  
  - Download formatted outputs (PPTs, PDFs, etc.)  

## ☁️ Platform
- Entire system is built on **Azure**, using **OpenAI models**  
- Orchestrated through a **Multi-Agent Framework** (e.g., LangGraph / CrewAI)
