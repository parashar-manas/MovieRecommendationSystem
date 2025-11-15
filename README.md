# Movie Recommendation System  

## Overview  
This solution delivers a lightweight, item-based collaborative filtering engine designed for scalable analytics environments. It analyzes user–item interaction patterns to compute item similarity and provide personalized movie recommendations. The architecture is engineered for modularity, rapid prototyping, and extensibility into production-grade recommendation pipelines.

## Key Features  
- Item-based collaborative filtering powered by cosine similarity  
- Automated construction of a user–item ratings matrix  
- Configurable top-N recommendation output  
- Structured train/test segmentation for evaluation  
- Clean, modular codebase supporting iterative development  
- Dataset-agnostic design aligned with MovieLens-style schemas  

## Dataset Requirement  

### **ratings.csv**
| Column   | Description                    |
|----------|--------------------------------|
| userId   | Unique user identifier         |
| movieId  | Unique movie identifier        |
| rating   | User-assigned rating score     |
| timestamp| Rating event timestamp         |

### **movies.csv**
| Column  | Description            |
|---------|-------------------------|
| movieId | Unique movie identifier |
| title   | Movie title             |
| genres  | Genre metadata          |

## Workflow Architecture  
1. Load ratings and movie metadata  
2. Merge datasets into a unified analytics frame  
3. Remove non-essential metadata fields  
4. Build a user–item matrix using pivot operations  
5. Segment matrix into training and testing subsets  
6. Compute cosine-based item-to-item similarity  
7. Generate personalized recommendations using weighted similarity  

## Installation  

### 1. Clone the repository  
```bash
git clone <your-repo-url>
cd <project-folder>
