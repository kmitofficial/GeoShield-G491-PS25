# 🛡 GeoShield: AI-Driven Surveillance of Defense Zones
###### Zero-shot defense surveillance using vision-language models to detect unusual constructions, movements, or land-use changes in satellite imagery.

### ✔️ Overview

GeoShield is an AI-powered surveillance system designed to support defense and intelligence by analyzing satellite imagery for unusual activities or constructions in border zones. Powered by Microsoft’s GeoVision Labeler (GVL) framework, it uses zero-shot learning to classify satellite images without any labeled training data.

By combining vision-language models (vLLMs) with large language models (LLMs), GeoShield generates interpretable image descriptions and detects potentially suspicious changes such as new buildings, roads, camps, or movements—even in data-scarce regions.

### ✔️ Features

- Zero-shot classification of satellite images using vLLMs + LLMs  
- Temporal comparison across images to detect land-use changes  
- Reasoning agent to flag and explain unusual or suspicious activities  
- Hierarchical semantic clustering of detected structures  
- Web dashboard for visual alerts and logs  
- Modular AI agent architecture using FastAPI and Docker  

> **Note:** The section below outlines the *planned* functionality of GeoShield. Implementation may vary depending on time, feasibility, and available resources.

### ✔️ Planned LLM Workflow

- **Image Preprocessing**  
  Uploaded satellite images are split into small patches (e.g., 256×256), each with an ID and geolocation metadata.

- **Patch Description via Vision LLM**  
  Each patch is processed by a vision-language model (e.g., Kosmos-2), which generates a natural language description of the scene (e.g., “a cluster of tents in an open field”).

- **Classification via Language Model**  
  The generated description is passed to a language model (e.g., LLaMA) that maps it to a defense-relevant label (e.g., “military camp”, “civilian structure”).  
  If the classification is ambiguous or fails, a fallback mechanism using CLIP directly classifies the image.

- **Change Detection & Reasoning**  
  If previous versions of the patch exist, the system compares classifications over time.  
  An LLM-based reasoning agent evaluates the change and flags it as either routine (e.g., seasonal farming) or suspicious (e.g., new helipads, camps).

### ✔️ Tech Stack

| **Component**              | **Technology Used**                 |
| -------------------------- | ----------------------------------- |
| **Frontend**               | React.js (MERN Stack Frontend)      |
| **Backend API**            | FastAPI / Express.js                |
| **Image Models**           | Kosmos-2, LLaMA-3.2 Vision-Instruct |
| **Language Models**        | Family of LLaMA                     |
| **Workflow Orchestration** | Python, Docker, LLM Agents          |
| **Database**               | MongoDB                             |

### ✔️ Use Cases

- Detecting new defense infrastructure near borders  
- Identifying illegal constructions or encampments  
- Monitoring land-use changes in restricted areas  
- Triggering alerts during surveillance operations  

### ✔️ Intended Users

- Defense and military surveillance teams  
- Border patrol and homeland security analysts  
- Government geospatial intelligence (GEOINT) units  
- Researchers in AI, remote sensing, and security  

### ✔️ Architecture Diagram

![Architecture Diagram](https://res.cloudinary.com/dur2vhjfv/image/upload/v1753890045/ArchitectureDiagramGeoShield_hdbfkj.jpg)

### ✔️ Workflow Diagram

<img src="https://res.cloudinary.com/dur2vhjfv/image/upload/v1753890012/WorkflowDiagramGEOSHIELD_ori0gt.png" height="800" width="600" />

### 👨‍💻 Contributors

- [@teja-ghankot](https://github.com/teja-ghankot)  
- [@samarpanelipay](https://github.com/samarpanelipay)  
- [@Sri-Teja-1](https://github.com/Sri-Teja-1)  
- [@pranavkumarjangam](https://github.com/pranavkumarjangam)  
- [@ravikirankachiraju](https://github.com/ravikirankachiraju)
