# 🧬 Breast Cancer Survival Prediction, Subtype Classification, and Generative Modeling Using TCGA RNA-Seq Data

📄 **Project Documentation**: [View full documentation](https://docs.google.com/document/d/1fS-jqSml-WKNthAajrXePv_-EIa3vYGGsH8jhxKzvFk/edit?tab=t.0#heading=h.cj81kr72oewr)

## 📘 Overview

This project analyzes breast cancer data from The Cancer Genome Atlas (TCGA) to support precision oncology through:

* ✅ **Survival Prediction**: Predicting 5-year overall survival based on RNA-Seq gene expression
* ✅ **Subtype Classification**: Identifying molecular subtypes of breast cancer
* ✅ **Data Generation**: Using generative models to simulate realistic gene expression profiles

## 🔍 Background

Breast cancer is the most diagnosed cancer and a leading cause of cancer-related death among women globally. This project explores the heterogeneity of breast cancer by leveraging:

* RNA-seq gene expression data
* Clinical metadata
* Machine learning methods like XGBoost
* Generative models such as Variational Autoencoders (VAEs)

## 📁 Data Sources

* **Clinical Data**: TCGA BRCA clinical metadata (TSV format)
* **RNA-Seq Data**: TCGA BRCA RNA-seq (RSEM log2 normalized, gzipped format)

## 🛠️ Technologies & Tools

* Python (pandas, scikit-learn, XGBoost, TensorFlow/Keras)
* Jupyter Notebook
* Matplotlib / Seaborn for visualization

## 🚀 How to Run

1. Clone the repo:

   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook:
   Open `Project2.ipynb` in Jupyter Lab or Notebook environment and execute the cells.

## 📊 Sample Code Snippet

```python
# Load clinical and RNA-seq data
clinical_df = pd.read_csv(clinical_path, sep="\t", low_memory=False)
rnaseq_df = pd.read_csv(rnaseq_path, sep="\t", compression="gzip")

# Set gene names as index and transpose so samples become rows
rnaseq_df = rnaseq_df.set_index('attrib_name').transpose()
```

## 🧠 Machine Learning Goals

* Classification: Molecular subtype detection
* Survival Analysis: Gradient boosting for 5-year outcome prediction
* Generative Modeling: Variational Autoencoders for synthetic gene profile creation

## 📌 Future Improvements

* Integrate additional clinical parameters
* Enhance model interpretability with SHAP
* Use external validation cohorts

## 📜 License

MIT License
