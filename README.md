# Azure Video Insights

A comprehensive demonstration project showcasing Azure's video analysis capabilities through both Azure AI Content Understanding and Azure Video Indexer services. This repository provides practical implementations, comparisons, and integration examples for AI-powered video analytics solutions.

## 🔍 Service Comparison

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

## 🛠️ Installation and Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/AzureVideoInsights.git
   cd AzureVideoInsights
   ```

2. **Install dependencies**:
   ```bash
   pip install azure-ai-documentintelligence
   pip install azure-storage-blob
   pip install azure-search-documents
   pip install azure-identity
   pip install openai
   pip install python-dotenv
   pip install requests
   ```

3. **Configure environment**:
   - Copy `.env.example` to `.env`
   - Fill in your Azure service credentials

4. **Prepare sample data**:
   - Place your video files in the `data/` directory
   - Update file paths in the notebooks

