# **🛡 GeoShield: AI-Driven Surveillance of Defense Zones**

###### Zero-shot defense surveillance using vision-language models to detect unusual constructions, movements, or land-use changes in satellite imagery.



### **✔️ Overview**

GeoShield is an AI-powered surveillance system designed to support defense and intelligence by analyzing satellite imagery for unusual activities or constructions in border zones. Powered by Microsoft’s GeoVision Labeler (GVL) framework, it uses zero-shot learning to classify satellite images without any labeled training data.



By combining vision-language models (vLLMs) with large language models (LLMs), GeoShield generates interpretable image descriptions and detects potentially suspicious changes such as new buildings, roads, camps, or movements, even in data-scarce regions.



### **✔️ Features**

1. Zero-shot classification of satellite images using vLLMs + LLMs
2. Temporal comparison across images to detect land-use changes
3. Reasoning agent to flag and explain unusual or suspicious activities
4. Hierarchical semantic clustering of detected structures
5. Web dashboard for visual alerts and logs
6. Modular AI agent architecture using FastAPI and Docker





**Note:** Below section outlines the planned functionality of GeoShield. Implementation may vary depending on time, feasibility, and available resources. The README will be updated as development progresses.



### **✔️ Planned LLM Workflow**

1. *Image Preprocessing*
Uploaded satellite images are split into small patches (e.g., 256×256), each with an ID and location.
2. *Patch Description via Vision LLM*
   Each patch is processed by a vision-language model (e.g., Kosmos-2), which generates a natural language description of the scene.
3. *Classification via Language Model* 
   The description is passed to an LLM that maps it to a defense-relevant label (e.g., “military camp”).
   If the label is invalid, a CLIP fallback is used for direct image classification.
4. *Change Detection \& Reasoning*
    If a previous classification exists, the system compares labels over time.
    An LLM-based reasoning agent decides if the change is routine or suspicious.













### **✔️ Tech Stack**



| **Component**              | **Technology Used**                 |
| -------------------------- | ----------------------------------- |
| **Frontend**               | React.js (MERN Stack)               |
| **Backend API**            | FastAPI                             |
| **Image Models**           | Kosmos-2, LLaMA-3.2 Vision-Instruct |
| **Language Models**        | Family of LLaMA                     |
| **Workflow Orchestration** | Python, Docker, LLM Agents          |
| **Database**               | MongoDB                             |




### **✔️ Use Cases**

1. Detecting new defense infrastructure near borders
2. Identifying illegal constructions or encampments
3. Monitoring land-use changes in restricted areas
4. Triggering alerts during surveillance operations

### 

### **✔️ Intended Users**

1. Defense and military surveillance teams
2. Border patrol and homeland security analysts
3. Government geospatial intelligence (GEOINT) units
4. Researchers in AI, remote sensing, and security

### **✔️ Architecture Diagram**

![Architecture Diagram](https://res.cloudinary.com/dur2vhjfv/image/upload/v1753890045/ArchitectureDiagramGeoShield_hdbfkj.jpg)


### **✔️ Workflow Diagram**


<img src="https://res.cloudinary.com/dur2vhjfv/image/upload/v1753890012/WorkflowDiagramGEOSHIELD_ori0gt.png" height="800" width="600"/>



### **👨‍💻👨‍💻Contributors**
- [@teja-ghankot](https://github.com/teja-ghankot)
- [@samarpanelipay](https://github.com/samarpanelipay)
- [@Sri-Teja-1](https://github.com/Sri-Teja-1)
- [@pranavkumarjangam](https://github.com/pranavkumarjangam)
- [@ravikirankachiraju](https://github.com/ravikirankachiraju)




