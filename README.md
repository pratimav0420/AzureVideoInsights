# 🎬 Chat with Your Videos - AI-Powered Video Intelligence Platform

Transform your video content into an intelligent, searchable, and conversational experience! This comprehensive platform leverages Azure's cutting-edge AI services to extract deep insights from videos and enables natural language conversations about your content.

## ✨ What You Can Do

🗣️ **Chat with Videos** - Ask questions about your video content in natural language  
🔍 **Smart Discovery** - Find specific moments, topics, and insights across your video library  
🎯 **Intelligent Search** - Semantic search powered by AI embeddings for precise content discovery  
📊 **Rich Analytics** - Extract faces, emotions, topics, keywords, and detailed transcripts  
🚀 **Production Ready** - Compare Azure AI Content Understanding vs Video Indexer for your use case  

## 🎯 Key Features

- **Conversational Video Interface**: Ask "What did they discuss about budgets?" or "Show me when John appeared"
- **Semantic Video Search**: Find content by meaning, not just keywords
- **Multi-Modal Analysis**: Process video, audio, and visual elements simultaneously  
- **Real-time Insights**: Extract faces, objects, emotions, topics, and sentiment analysis
- **Enterprise Ready**: Production-grade implementation with Azure's enterprise services
- **Flexible Architecture**: Choose between Azure AI Content Understanding (Preview) or Video Indexer (GA)

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

## 🚀 How It Works - From Video to Conversation

```
📹 Upload Video  →  🤖 AI Analysis  →  💬 Natural Chat  →  🎯 Instant Answers
```

**1. Upload & Process** 📤  
Drop your video files into Azure Storage and let AI extract every detail

**2. Intelligent Analysis** 🧠  
Advanced AI models analyze speech, visuals, emotions, and context

**3. Ask Anything** 💭  
"What were the key decisions made?"  
"When did the speaker mention quarterly results?"  
"Show me all instances of product demonstrations"

**4. Get Instant Insights** ⚡  
Receive precise answers with timestamps and relevant video segments

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

