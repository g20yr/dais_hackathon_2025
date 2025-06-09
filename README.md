# Accessible Travel Agent

Databricks Data + AI Summit 2025

---

## Overview

The **Accessible Travel Agent** demo empowers travelers with disabilities to plan multi-day, fully accessible trips in seconds. Leveraging Databricks for data processing, Llama 4 for language understanding, and LangChain for agent orchestration, this project generates personalized itineraries based on user-specified accessibility needs.

## Features

- **Custom Itinerary Generation**: Specify accessibility requirements (e.g., step-free routes, sign language support, sensory-friendly attractions) to receive a detailed travel plan.
- **Data-Driven Recommendations**: Aggregates hotel, attraction, and transit data from Delta tables in Unity Catalog.
- **Scalable Model Deployment**: Built-in MLflow integration for seamless model logging, versioning, and serving in Databricks.
- **Modular Agent Framework**: LangChain-based architecture allowing easy extension with new data sources or booking APIs.

## Architecture

1. **Data Layer**: Delta Lake tables stored in Unity Catalog for hotels, attractions, transit, and accessibility features.
2. **Notebook Workflows**: PySpark notebooks preprocess and join data, exposing it to the agent.
3. **Agent Layer**: LangChain agents call custom tools to query Databricks SQL and format responses.
4. **Model Layer**: Llama 4 model handles natural language understanding and itinerary synthesis.
5. **Serving Layer**: MLflow model registry and serving endpoints provide real-time itinerary generation.

## Prerequisites

- Databricks workspace with Unity Catalog enabled
- Cluster with access to Delta tables and MLflow
- Python dependencies: `langchain`, `databricks-sdk`, `mlflow`, `pandas`
- API credentials (for future booking integrations)

## Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/g20yr/dais_hackathon_2025.git
