# Azure AI Content Understanding Setup Guide

This guide provides comprehensive instructions for setting up Azure AI Content Understanding service with complete workflow covering prebuilt analyzers, custom analyzer creation, video analysis, and Azure AI Search integration.

## 🎯 Complete Workflow Overview

```mermaid
graph TB
    A[Video File] --> B[Azure AI Content Understanding]
    B --> C{Analyzer Type}
    C -->|Prebuilt| D[Prebuilt Video Analyzer]
    C -->|Custom| E[Custom Analyzer Creation]
    D --> F[GPT-4 Powered Analysis]
    E --> G[Custom Schema Processing]
    F --> H[Extract Rich Insights]
    G --> H
    H --> I[Generate Embeddings]
    I --> J[Azure AI Search Index]
    J --> K[Semantic Search & Chat]
    
    subgraph "Content Understanding Features"
        L[Multimodal Analysis]
        M[Custom Field Schemas]
        N[Face Detection & Grouping]
        O[Emotion & Sentiment Analysis]
        P[Topic & Keyword Extraction]
    end
    
    classDef primary fill:#0078d4,stroke:#ffffff,stroke-width:2px,color:#ffffff
    classDef processing fill:#881798,stroke:#ffffff,stroke-width:2px,color:#ffffff
    classDef storage fill:#107c10,stroke:#ffffff,stroke-width:2px,color:#ffffff
    
    class B,D,E primary
    class F,G,H,I processing
    class J,K storage
```

## 📋 Prerequisites

### Required Azure Services

1. **Azure AI Services** - For Content Understanding capabilities
2. **Azure AI Search Service** - For indexing and searching insights
3. **Azure OpenAI Service** - For embeddings and enhanced processing
4. **Azure Active Directory** - For authentication and authorization

### Required Permissions

- Content Understanding API access
- Azure AI Search contributor access
- Azure OpenAI API access
- Azure Storage access (if using blob storage)

## 🚀 Step 1: Azure AI Content Understanding Service Setup

### 1.1 Create Azure AI Services Resource

1. **Navigate to Azure Portal**
   - Go to [Azure Portal](https://portal.azure.com)
   - Click "Create a resource" → "AI + Machine Learning" → "Azure AI services"

2. **Configure Basic Settings**
   ```
   Subscription: Your subscription
   Resource Group: Create new or use existing
   Region: Supported region (East US, West Europe, etc.)
   Name: content-understanding-service
   Pricing Tier: S0 (Standard)
   ```

3. **Enable Content Understanding**
   - After creation, navigate to your AI Services resource
   - Go to "Resource Management" → "Features"
   - Enable "Content Understanding (Preview)"

### 1.2 Get Service Credentials

```bash
# Get the endpoint and keys
az cognitiveservices account show --name content-understanding-service --resource-group myResourceGroup
az cognitiveservices account keys list --name content-understanding-service --resource-group myResourceGroup
```

Save these values for your `.env` file:
- Endpoint URL
- Primary API Key
