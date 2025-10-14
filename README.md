# Overview


  This project revolves around the soccer transfer market that has been anything but steady after the unprecedented transfer of Neymar Jr. from F.C Barcelona for over 200 million euros. Unforunately, this landmark transfer started a trend in which players were overvalued for their contributions on the soccer field. In order to combat this problem, this project works to correct the transfer market by creating a transfer valuation standard related to performance and age.  


## Data

  The data related to player performance was webscraped via the worldfootballR package which contained data from FBref, a website with different markers related to Offense, Midfield, and Defense

    Offense Dataset  - Included stats relevant to forwards ( goals, shots, expected goals).
      

    Midfield Dataset - Focused on playmaking metrics (e.g., assists, key passes, progressive passes).

    Defense Dataset - Included stats such as tackles, interceptions, and blocks.


## Methodology

  ### Correlation Tests and Feature Selection
      
      A Pearson correlation threshold was used to filter high-impact variables:

        For offensive players, metrics such as Goals + Assists (G+A), Expected Contribution (xG + xAG), and total shots were strongly correlated with value.
        For midfielders, top features included Assists, Key Passes, Progressive Passes, and xAG.
        For defenders, stats like Tackles in the Attacking Third, Pass Blocks, and Clearances were selected.


  ### Modeling 

      Linear Regression

          Linear regression was chosen for its ability to expose direct linear relationships between features and market value. Both raw value and log-transformed
      value models were tested. Log transformation was applied to stabilize variance and manage skewed distributions.
    
      Random Forest Regression
        
          Random Forest Regression was used to capture nonlinear relationships and feature interactions. Random Forest models tend to perform better when the 
      relationship between inputs and target is complex or hierarchical. They also provide feature importance metrics, which were visualized to understand which stats most influenced         predictions.

  

## Results

    Final app produced in streamlit. 

## Citations

  Zivkovic J (2022). _worldfootballR: Extract and Clean World Football (Soccer) Data_. R package version
  0.6.2, <https://CRAN.R-project.org/package=worldfootballR>.
  How does a football transfer work? (2022, February 25). https://www.bbc.com/worklife/article/20170829-how-does-a-football-transfer-work
  Transfermarkt. (n.d.). Football transfers, rumours, market values and news. https://www.transfermarkt.com/



