# Public Transport Clustering Project

## Overview
This project applies **K-Means clustering** to analyze public transport data, identifying meaningful groupings based on various attributes such as origin, destination, train type, train class, fare, and price.

## Dataset
The dataset contains public transport details with the following key attributes:
- `origin`: Departure location
- `destination`: Arrival location
- `train_type`: Type of train service
- `train_class`: Class of service
- `fare`: Ticket price category
- `price`: Actual fare amount
- `insert_date`, `start_date`, `end_date`: Dates related to the record (removed for clustering)

## Preprocessing Steps
1. **Dropped unnecessary columns**: `Unnamed: 0`, `insert_date`, `start_date`, and `end_date`
2. **Handled missing values**: Replaced missing `price` values with the median
3. **Encoded categorical variables** using `LabelEncoder`

## Clustering Approach
- Used **K-Means Clustering** to segment the data
- Determined the optimal number of clusters using the **Elbow Method**
- Applied K-Means with the chosen number of clusters
- Saved the clustered dataset for further analysis

## Files
- `public_transport.csv` - Original dataset
- `clustered_public_transport.csv` - Clustered dataset
- `kmeans_model.pkl` - Trained K-Means model (if saved)
- `clustering_script.py` - Python script for clustering (modify path if needed)

## How to Run
1. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib scikit-learn
   ```
2. Run the script:
   ```bash
   python clustering_script.py
   ```
3. View the `Elbow Method` plot to determine the best `K`
4. Use the generated `clustered_public_transport.csv` for analysis

## Future Improvements
- Use **Silhouette Score** for better cluster evaluation
- Try **Hierarchical Clustering** for comparison
- Implement **real-time clustering** for new data

## Author
Shuaib

---
🚀 Happy Clustering!

