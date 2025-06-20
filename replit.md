# Hierarchical Federated Learning Platform

## Overview

This is a comprehensive Streamlit-based hierarchical federated learning platform designed for diabetes prediction using healthcare data. The system implements a 3-tier federated learning architecture (Patient → Fog → Global) with advanced security mechanisms, differential privacy, and real-time visualization capabilities.

## System Architecture

### Frontend Architecture
- **Framework**: Streamlit web application with interactive dashboard
- **Language**: Python with extensive use of Plotly for visualizations
- **UI Components**: Multi-tab interface with real-time progress tracking
- **Internationalization**: Built-in translation support (English/French)

### Backend Architecture
- **Core Engine**: Custom federated learning orchestrator (`FederatedLearningManager`)
- **Client Simulation**: Multi-threaded client simulators with various ML models
- **Aggregation Layer**: Multiple algorithms (FedAvg, FedProx, WeightedAvg, Median)
- **Security Layer**: Committee-based validation with cryptographic proofs

### Data Processing Pipeline
- **Preprocessing**: Custom `DataPreprocessor` with scaling and imputation
- **Distribution Strategies**: IID, Non-IID (Dirichlet, pathological, quantity skew)
- **Privacy Protection**: Differential privacy with Gaussian, Laplace, and Exponential mechanisms

## Key Components

### Core Modules
1. **`app.py`** - Main Streamlit application with multi-tab interface
2. **`federated_learning.py`** - Central FL orchestrator with training coordination
3. **`client_simulator.py`** - Individual client simulation with local training
4. **`fog_aggregation.py`** - Hierarchical fog node management and aggregation
5. **`aggregation_algorithms.py`** - Implementation of various FL aggregation methods

### Security & Privacy
1. **`committee_security.py`** - Byzantine-fault tolerant committee system
2. **`differential_privacy.py`** - Multiple DP mechanisms with privacy accounting
3. **`training_secret_sharing.py`** - Shamir's secret sharing for model weights

### Data & Analytics
1. **`data_preprocessing.py`** - Comprehensive data cleaning and feature engineering
2. **`data_distribution.py`** - Various data distribution strategies for FL clients
3. **`client_visualization.py`** - Real-time client performance monitoring
4. **`advanced_client_analytics.py`** - Advanced analytics and anomaly detection

### Visualization & UX
1. **`journey_visualization.py`** - Interactive user journey tracking
2. **`performance_optimizer.py`** - Intelligent performance recommendations
3. **`translations.py`** - Multi-language support system

## Data Flow

### Training Flow
1. **Data Loading**: Loads diabetes.csv dataset with medical features
2. **Preprocessing**: Handles missing values, scaling, and feature engineering
3. **Client Distribution**: Distributes data across simulated medical stations
4. **Local Training**: Each client trains on local data using selected ML model
5. **Fog Aggregation**: Fog nodes aggregate client updates using chosen algorithm
6. **Global Convergence**: Global model updates from fog node aggregations
7. **Evaluation**: Real-time metrics tracking and convergence monitoring

### Security Flow
1. **Committee Formation**: Dynamic committee selection with reputation scoring
2. **Update Validation**: Committee validates client updates for Byzantine faults
3. **Privacy Protection**: Differential privacy applied to model parameters
4. **Secret Sharing**: Model weights divided using Shamir's secret sharing

## External Dependencies

### Core Dependencies
- **Streamlit**: Web application framework
- **NumPy/Pandas**: Data manipulation and numerical computing
- **Scikit-learn**: Machine learning models and metrics
- **Plotly**: Interactive visualizations and dashboards

### Specialized Libraries
- **Cryptography**: Cryptographic operations for security protocols
- **ReportLab**: PDF documentation generation
- **NetworkX**: Graph-based committee management
- **Matplotlib/Seaborn**: Statistical visualizations

### Development Stack
- **Node.js/TypeScript**: Full-stack setup with React frontend capability
- **Drizzle ORM**: Database management (configured for PostgreSQL)
- **Vite**: Build tooling and development server
- **Tailwind CSS**: Styling framework

## Deployment Strategy

### Development Environment
- **Replit Integration**: Configured for Replit development environment
- **Hot Reload**: Vite-powered development with live updates
- **Port Configuration**: Streamlit runs on port 5000, Vite on development port

### Production Deployment
- **Build Process**: Multi-stage build with frontend compilation
- **Autoscale Target**: Configured for automatic scaling
- **Health Checks**: Built-in health monitoring and error handling

### Database Strategy
- **PostgreSQL**: Primary database with Drizzle ORM
- **Schema Management**: Automated migrations and type-safe queries
- **Connection Pooling**: Optimized for concurrent federated learning operations

## Changelog

```
Changelog:
- June 18, 2025. Initial setup
```

## User Preferences

```
Preferred communication style: Simple, everyday language.
```