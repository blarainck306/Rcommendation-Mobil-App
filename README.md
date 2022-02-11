# Rcommendation-Mobil-App

## Model Class
- WDL_FTRL_model.py : wide and deep model class, see [github](https://github.com/blarainck306/WDL_FTRL) for different model class definitions for the purposes of wide only training, deep only training, combined training, and using optimizations of OGD and FTRL-proximal etc.

## Utility
- utility.py: utility functions used by ipython notebooks

## ETL,EDA, Preprocessing
- 0_etl-AvazuCTR.ipynb: spark, look at data schema, convert csv to parquet 
- 0_sql-AvazuCTR_plot: EDA, analytical queries based on spark sql
- 1_SparkProcess_AvazuCTR_withDash: data engineering in Spark
- 2_make_petastorm_loader_wDash: make a Pytorch dataloader out of parquet files

## Model Training
### Train wide deep respectively 
- 3_OGD_L2Wide_DeepOnly: Wide & Deep model training on the deep part 
- 3_OGD_L2Wide_WideOnly: Wide & Deep model training on the wide part using the online gradient descent/stochastic gradient descent

### Joint training

- 4_OGD_L2Wide_Combine:training model with preloaded weights from previous '3_OGD_L2Wide_DeepOnly' and '3_OGD_L2Wide_WideOnly'
- 4_OGD_L2Wide_Combine_addRegu.ipynb: added regularization on the deep side after training above in '4_OGD_L2Wide_Combine'


