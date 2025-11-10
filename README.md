# CiteConnect: Research Paper Recommendation System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Code Coverage](https://img.shields.io/badge/coverage-85%25-brightgreen.svg)](https://github.com/DhikshaMathanagopal/CiteConnect)

## 🎯 Overview

CiteConnect is an intelligent research paper recommendation system that combines **retrieval-augmented generation (RAG)**, **vector search**, and **citation graph analysis** to help researchers efficiently discover and explore relevant academic literature. Unlike traditional keyword-based search engines, CiteConnect provides curated recommendations with explanations and visualizes connections through interactive citation graphs.

## 🚀 Key Features

- **Semantic Search**: Advanced vector-based retrieval using SPECTER2 embeddings for finding relevant papers beyond keyword matching
- **Citation Network Visualization**: Interactive graph visualization showing connections between papers
- **Personalized Recommendations**: User profiles that adapt to individual research interests over time
- **Explainable Results**: LLM-generated summaries explaining why each paper is relevant
- **Multi-Database Architecture**: Integrated storage using PostgreSQL, Neo4j, Vector DB, and Redis
- **Production-Ready MLOps**: Complete CI/CD pipeline with monitoring, versioning, and automated deployment

## 👥 Team

- **Abhinav Aditya**
- **Anusha Srinivasan**
- **Dennis Jose**
- **Dhiksha Mathanagopal**
- **Sahil Mohanty**

## 📊 Dataset

- **Size**: 10,000-20,000 papers initially (scalable to 100,000+)
- **Sources**: 
  - [arXiv API](https://info.arxiv.org/help/api/)
  - [Semantic Scholar API](https://www.semanticscholar.org/product/api)
  - [Unpaywall](https://unpaywall.org/products/api)
- **Storage**: ~2MB per PDF (20-40GB total for 20K papers)
- **Format**: JSON metadata, PDF papers, embeddings, citation graphs

## 🏗️ Architecture

### Technology Stack

**Infrastructure & Deployment**
- Google Cloud Platform (GCP)
- Kubernetes for container orchestration
- Docker for containerization
- Apache Airflow for pipeline orchestration

**Data Storage**
- PostgreSQL: Metadata storage
- Neo4j: Citation graph database
- Weaviate/FAISS: Vector embeddings
- Redis: Caching layer
- Google Cloud Storage: Raw PDF storage

**ML/AI Components**
- SPECTER2: Academic paper embeddings
- OpenAI API: Summarization and explanation generation
- sentence-transformers: Backup embedding models

**Monitoring & MLOps**
- Prometheus: Metrics collection
- Grafana: Visualization dashboards
- MLflow: Experiment tracking and model versioning
- DVC: Data version control
- Cloud Logging: Centralized logging

## 🎯 Performance Targets

### Technical Metrics
- **Recall@10**: ≥ 0.75
- **Precision@10**: ≥ 0.60
- **Query Latency (p95)**: < 2 seconds
- **System Availability**: 99.5%
- **Code Coverage**: 85%+

### User Engagement
- **Click-Through Rate**: ≥ 25%
- **Return User Rate (7-day)**: ≥ 35%
- **Average Session Duration**: ≥ 10 minutes

## 🚀 Getting Started

### Prerequisites

```bash
# Required software
- Python 3.9+
- Docker & Docker Compose
- Google Cloud SDK
- Node.js (for frontend)
```

### Installation

```bash
# Clone the repository
git clone https://github.com/DhikshaMathanagopal/CiteConnect.git
cd CiteConnect

# Set up virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your API keys and configuration
```

### Docker Setup

```bash
# Build and start services
docker-compose up -d

# Verify services are running
docker-compose ps
```
