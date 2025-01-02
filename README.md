# **End-to-End Recommendation Pipeline**

This project implements a comprehensive **End-to-End Recommendation Pipeline** that combines embedding models, transformer-based ranking, and multi-armed bandit algorithms to deliver personalized content recommendations. Designed with modularity in mind, the pipeline supports dynamic updates and integrates seamlessly with new datasets and use cases.

---

## **Project Structure**

### **Code Directory**
Below is a brief description of each `.py` file in the `code/` directory:

- **`candidate_generators.py`**: Implements popular and custom recommender algorithms.
- **`classification.py`**: Handles classification tasks within the pipeline.
- **`clustering.py`**: Provides clustering utilities for grouping similar items or users.
- **`data_loader.py`**: Loads and validates data files for use in the pipeline.
- **`data_preparation.py`**: Prepares and preprocesses raw data for embedding and ranking models.
- **`embedding_utils.py`**: Utilities for working with embeddings, including transformations and computations.
- **`embeddings.py`**: Manages the creation and handling of user and content embeddings.
- **`features_processing.py`**: Processes user and content features for model input.
- **`file_operations.py`**: Handles file input/output operations.
- **`main_cold_start.py`**: Manages recommendations for new (cold-start) users.
- **`main_final_ranking.py`**: Executes the final ranking stage of the pipeline.
- **`main_offline.py`**: Runs the offline embedding and ranking pipeline.
- **`main_online.py`**: Manages the online recommendation workflow.
- **`main_precompute.py`**: Precomputes embeddings for users and content.
- **`main.py`**: Entry point for running the complete pipeline.
- **`multi_armed_bandit.py`**: Implements epsilon-greedy strategies for dynamic exploration and exploitation.
- **`online_ranking.py`**: Handles ranking content using embedding and transformer models.
- **`pv_embedding_training.py`**: Trains the pairwise embedding (PV) model.
- **`recommender.py`**: Integrates multiple recommendation strategies into a unified framework.
- **`sequence_preparation.py`**: Prepares training sequences for the transformer ranking model.
- **`simulate_interaction.py`**: Simulates user-content interactions for training and evaluation.
- **`test_data_preparation.py`**: Prepares test users and content for predictions.
- **`text_clustering.py`**: Provides clustering utilities for text data.
- **`transformer_training.py`**: Trains the transformer model for content ranking.
- **`user_engagement_processor.py`**: Processes user engagement data for model input.
- **`user_model.py`**: Builds and trains the user embedding model.
- **`visualization.py`**: Visualizes data insights, model outputs, and recommendations.
- **`setup.py`**: Contains project setup configuration for installation.

---

### **Data Directory**
The `data/` directory contains the following files:

1. **Input and Preprocessed Data**:
   - `aggregated_user.csv`: Aggregated user data for engagement metrics.
   - `content_final.csv`: Final processed content-level input data.
   - `processed_content.csv`: Preprocessed content embeddings and metadata.
   - `processed_user_test.csv`: Processed features for test users.
   - `taxonomy_engagement_data.csv`: Raw engagement data for training and evaluation.
   - `to_predict_on.csv`: Test user and content IDs for predictions.

2. **Model Files**:
   - `content_model.pth`: Trained content embedding model.
   - `pv_model.pth`: Trained PV embedding model.
   - `transformer_model.pth`: Trained transformer ranking model.
   - `user_model.pth`: Trained user embedding model.

3. **Intermediate and Output Files**:
   - `vg2595_offline_data.pkl`: Precomputed embeddings for users and content.
   - `generated_content.pkl`: Serialized recommended content IDs.
   - `vg2595_recommended_items.txt`: Final recommended items for users.

---

## **How to Run**

### **1. Installation**

#### Using `install_dependencies.py`:
```bash
python install_dependencies.py
```

---

### **2. Running Main Scripts**

#### **Offline Training**
Train the PV embedding model and transformer model:
```bash
python code/main_offline.py
```

#### **Precomputing Embeddings**
Generate precomputed embeddings for users and content:
```bash
python code/main_precompute.py
```

#### **Online Recommendations**
Run the online recommendation pipeline:
```bash
python code/main_online.py
```

#### **Cold-Start Recommendations**
Generate recommendations for new users:
```bash
python code/main_cold_start.py
```

#### **Final Ranking**
Execute the final ranking stage for content:
```bash
python code/main_final_ranking.py
```

---

## **Key Features**
- **Modular Design**: Each component is self-contained for easy updates and customization.
- **Scalable Architecture**: Handles large datasets with precomputed embeddings and efficient ranking models.
- **Advanced Techniques**: Combines PV embeddings, transformer-based ranking, and multi-armed bandit exploration.

---

## **Contributing**
Contributions are welcome! Follow these steps:
1. Fork the repository.
2. Create a feature branch.
3. Submit a pull request.

---

## **Acknowledgements**
This project was developed as part of an academic exploration into advanced recommendation systems.

---

## **License**
This project is licensed under the MIT License.
