# Movie Recommendation System  

A Lightweight Item-Based Collaborative Filtering Engine
This repository provides a modular, analytics-ready movie recommendation pipeline built using **Pandas**, **Scikit-Learn**, and **NumPy**. The solution implements **item-based collaborative filtering**, enabling personalized movie recommendations based on user-rating similarity patterns. The project is optimized for clarity, maintainability, and extensibility, making it suitable for experimentation and production-oriented prototyping.

---

## Overview  

The project operationalizes a fundamental movie recommendation engine leveraging collaborative filtering. By analyzing user–item interactions through a user–movie ratings matrix and calculating cosine similarity between items, the system produces curated recommendations tailored to individual users.

This approach is well-suited for cold-start mitigation, platform analytics, and scalable recommendation pipelines.

---

## Key Features  

- **Item-based Collaborative Filtering** using cosine similarity  
- **User–Item Matrix Generation** from merged ratings and movies datasets  
- **Configurable Recommendation Output** (top-N suggestions)  
- **Training/Test Split** for evaluation or experimentation  
- **Clean and understandable code structure** for rapid iteration  
- **Dataset-agnostic design** compatible with any MovieLens-format data  

---

## Technology Stack  

| Component | Description |
|----------|-------------|
| **Pandas** | Data wrangling and preprocessing |
| **Scikit-Learn** | Cosine similarity computation |
| **NumPy** | Matrix operations and transformations |
| **Python 3.x** | Execution environment |

---

## Dataset Requirements  

The system expects two CSV files:

### **1. `ratings.csv`**
| Column | Description |
|--------|-------------|
| `userId` | Unique identifier for users |
| `movieId` | Unique identifier for movies |
| `rating` | User’s rating value |
| `timestamp` | Rating timestamp |

### **2. `movies.csv`**
| Column | Description |
|--------|-------------|
| `movieId` | Unique movie identifier |
| `title` | Movie title |
| `genres` | Genre tags |

These match the MovieLens datasets but can be adapted to similar schemas.

---

## Workflow Architecture  

The pipeline follows a structured flow:

1. **Load ratings and movie metadata**
2. **Merge both datasets**
3. **Remove unused metadata columns**
4. **Construct a user–item matrix using pivoting**
5. **Split matrix into training and testing subsets**
6. **Compute item–item cosine similarity**
7. **Generate recommendations using similarity weighting**

This ensures a robust analytical foundation supporting further extensions such as normalization, hybrid models, or implicit feedback integration.

---

## Installation  

### 1. Clone the repository  
```bash
git clone <your-repo-url>
cd <project-folder>
