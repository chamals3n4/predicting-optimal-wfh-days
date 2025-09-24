## Predicting Optimal WFH Days to Maximize Productivity

### Overview
This project was done as part of the IT2011 Group Assignment (Data Preprocessing & Exploratory Data Analysis). Its objective is to predict the optimal number of work-from-home (WFH) days—categorized as Low, Medium, or High—to maximize employee productivity.

The project includes:
- Using a remote worker dataset.
- Applying a full preprocessing and EDA pipeline.
- Preparing a clean, structured feature set for downstream modeling.
- Organizing work into modular notebooks, with each notebook aligned to specific team member responsibilities.

### Dataset
- **Name**: remote_work_productivity.csv  
- **Source**: [Hugging Face – Remote Worker Productivity](https://huggingface.co/datasets/nprak26/remote-worker-productivity/raw/main/remote_work_productivity.csv)  
- **Original size**: 1,500 rows, 32 columns  
- **After preprocessing**: 1,131 rows, 13 columns

### Features and Target (post-processing)
- **Selected features**: `Age`, `Productivity_Score`, `Meetings_Per_Week`, `Job_Satisfaction`, `Has_Children_Yes`, `Location_Type_Suburban`, `Location_Type_Urban`, `Department_Group`, `Education_Group`, `Job_Level_Group`, `Company_Size_Group`
- **Target**: `WFH_Category` with classes: Low, Medium, High

### Project Structure
- `data/remote_work_productivity.csv` – Raw dataset (downloaded from source)
- `notebooks/` – Modular notebooks for each pipeline stage
  - `01_missing_data_handling.ipynb`
  - `02_categorical_encoding.ipynb`
  - `03_outlier_detection_removal.ipynb`
  - `04_data_normalization_scaling.ipynb`
  - `05_feature_engineering.ipynb`
  - `06_feature_selection_dimensionality.ipynb`
  - `group_pipeline.ipynb` – Combines the entire pipeline into one workflow
- `results/`
  - `eda_visualizations/` – Saved figures from EDA and transformations
  - `outputs/final_preprocessed.csv` – Final preprocessed dataset

### Group Members
- **IT24103927 Hettiarachchi H.S.A.** -  Handling missing data
- **IT24103918 Wagawala W.L.U.N.** -  Encoding categorical variables
- **IT24103913 Mahindarathne R.M.P.K.T.** -  Outlier removal
- **IT24103965 Shruthihan S.** -  Normalization/scaling
- **IT24103885 Senarathna Y.M.C.S.** -  Feature engineering
- **IT24103979 Hamshithan V.** -  Feature selection and dimensionality reduction

### How to Run
1. **Install prerequisites**
   - Python 3.8+ recommended
   - Install libraries:
     ```bash
     pip install pandas numpy scikit-learn seaborn matplotlib
     ```
2. **Open notebooks**
   - Launch Jupyter Lab/Notebook in the repository folder.
3. **Run the full pipeline**
   - Open `notebooks/group_pipeline.ipynb` and run all cells to process the data and generate the final CSV at `results/outputs/final_preprocessed.csv`.
4. **Explore individual steps (optional)**
   - Open each modular notebook in `notebooks/` to review and run the corresponding transformation step.

### Expected Outputs
- **Processed dataset**: `results/outputs/final_preprocessed.csv`
- **Visualizations**: saved under `results/eda_visualizations/` (e.g., `missing_values_heatmap.png`, `age_before_after_scaling.png`, `correlation_after_reduction.png`, etc.)

