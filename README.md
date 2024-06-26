# pediatric_cancer
Predictive Models for Pediatric Cancers

### information about the data and the structure of the data
# bulk RNA seq data is sourced from : https://www.sciencedirect.com/science/article/pii/S2211124721015333?via%3Dihub#bib20


# Get Started

1. Create Virtual Environment

    ```bash
    conda create -n pediatric_cancer python=3.9
    conda activate pediatric_cancer
    ```

2. Install requirements

    ```bash
    pip install -r requirements.txt
    ```

# Data
1. The data shared is stored in the `data/raw` directory
2. The data obtained from preprocessing is stored in `data/preprocessed`
    - `data/preprocessed/gene_expression_per_patient.csv`: Contains the preprocessed data of gene-expression corresponding to patients (column name used is Gene Name. Ensemble ID is skipped) originally obtained from `data/raw/sample_gene_expression_neuroblastoma.xlsx` and reading description from the file `data/raw/sample_gene_expression_neuroblastoma_README.xlsx`. Script used to process this is `notebooks/2. DataAnalysis_SampleGeneExpression.ipynb`. 
    - `data/preprocessed/patient_info_metadata.csv`: Contains the preproessed data of the patient metadata into (parsed the column names excluding patient's gene expression data) originally obtained from `data/raw/sample_gene_expression_neuroblastoma.xlsx` and reading description from the file `data/raw/sample_gene_expression_neuroblastoma_README.xlsx`. Script used to process this is `notebooks/2. DataAnalysis_SampleGeneExpression.ipynb`.
    - `data/preprocessed/patient_info_metadata_gene_expression.csv`: Contains the merged data from `data/preprocessed/gene_expression_per_patient.csv` and `/data/preprocessed/patient_info_metadata.csv`. Script used to process this is `notebooks/2. DataAnalysis_SampleGeneExpression.ipynb`. This data standalone can be used as a processed data for `data/raw/sample_gene_expression_neuroblastoma.xlsx` file. 

# Data Analysis

1. Jupyter notebooks in the `/notebook` directory are used for data analysis
    - `notebook/1. DataAnalysis_GeneMetaData.ipynb`: Use to analyse the `data/raw/gene_metadata_neuroblastoma.xlsx` and `/data/raw/gene_metadata_neuroblastoma_README.xlsx` files.
    - `notebook/2. DataAnalysis_SampleGeneExpression.ipynb`: Use to analyse the `data/raw/sample_gene_expression_neuroblastoma.xlsx` and `/data/raw/sample_gene_expression_neuroblastoma_README.xlsx` files.

