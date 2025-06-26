# AzureVideoInsights


# Azure AI Services Comparison

| **Capability** | **Azure AI Content Understanding (Preview)** | **Azure AI Video Indexer (GA)** |
|----------------|----------------------------------------------|----------------------------------|
| **Service Availability** | Public preview – evolving, no SLA. GA expected in 6 months. | Generally Available – production-ready with full support and SLAs. |
| **Supported Content Modalities** | Multimodal: documents, images, audio, video. | Video and audio focused; limited image/document support. |
| **Analysis Approach** | Segment-based generative analysis using GPT-4; customizable schema. | Frame-by-frame analysis with over 30 AI models. |
| **AI Models & Techniques** | Generative AI + Cognitive Skills; customizable outputs. | Pre-trained ML models; fixed metadata extraction. |
| **Output and Metadata** | Customizable schema; RAG-ready Markdown/JSON; whole-video summaries supported. | Predefined insights schema; AI-generated summary based on extracted metadata. |
| **Customization & Extensibility** | Highly customizable via Azure AI Foundry; supports custom analyzers and workflows. | Limited customization; mostly fine-tuning existing models. |
| **Face Recognition** | Supports face detection/grouping; custom person directory; generative celebrity ID. | Built-in celebrity recognition; account-specific face training. |
| **Summarization** | Segment-focused by default; whole-video summaries configurable. | Full video summary built-in using Azure OpenAI. |
| **Deployment Options** | Cloud-only (currently). | Cloud and Edge (via Azure Arc). |
| **Integration & Access** | APIs and Azure AI Studio (Foundry). | Web portal, APIs, SDKs, and embeddable widgets. |
| **Compliance & Security** | Limited compliance (preview); responsible AI considerations apply. | Certified for enterprise use (ISO, SOC, HIPAA, etc.); SLA-backed. |
