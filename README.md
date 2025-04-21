# 0421week9homework
title: "Subsidy Data Summary Report"
author: "Your Name"
date: "r Sys.Date()"
output: html_document

Data Description

This report is based on the dataset A21030000I-B13002-00W.csv, which records aggregated monthly observations of social insurance premium subsidies distributed across Taiwan. Each row in the dataset captures the total number of recipients and the total subsidy amount, disaggregated by demographic and geographic features including county, township, gender, age group, and subsidy type. The data span multiple months, and the structure allows for multivariate analyses by subgroup.

Variable definitions are detailed in the accompanying codebook. Key variables include:

保費年月 (premium_month): The reference month of subsidy issuance in YYYYMM format.

縣市 (county): County of residence.

鄉鎮 (town): Township of residence.

性別（男1女2） (gender): Binary gender indicator (1 = male, 2 = female).

補助項目 (subsidy_item): Code for the type of subsidy.

年齡區間 (age_group): Age group category.

補助人數 (people_count): Number of beneficiaries in the subgroup.

補助金額 (subsidy_amount): Total subsidy amount in New Taiwan Dollars (NTD).

The full codebook is provided in codebook_subsidy.json and codebook_subsidy.csv for reference and reproducibility.

Summary Statistics

Correlation Among Numeric Variables

A correlation analysis of the numeric variables is provided in correlation-matrix.json. The highest observed correlation is between 補助人數 and 補助金額, with a coefficient approaching unity, as expected given the subsidy mechanism is largely headcount-based. Other numeric variables exhibit low or negligible correlations.

Group Means by Gender

Summary statistics by gender are available in group-summary-by-sex.json. Both male and female groups receive subsidies, with slight differences in mean subsidy amounts and counts. These may reflect differences in demographic composition or policy reach by gender across regions.

Cross-Tabulation by County and Subsidy Type

The joint distribution of subsidy types across counties is documented in cross-tab-county-item.json. This cross-tab reveals substantial regional heterogeneity in program participation and the prevalence of specific subsidy items. Some counties are highly concentrated in a narrow range of subsidy types, while others distribute more broadly across categories.

Top Variables Correlated with Subsidy Amount

Finally, the strongest numeric predictors of 補助金額 are reported in top-correlated-with-amount.json. Unsurprisingly, 補助人數 tops the list, followed by other variables showing mild associations. These correlations provide useful inputs for further causal modeling and policy evaluation exercises.

Conclusion

The structure and granularity of the data make it well-suited for analyzing subsidy targeting, equity, and regional distribution in Taiwan. Combined with machine-readable summaries and a transparent codebook, this dataset is ready for econometric analysis, policy evaluation, and public accountability assessments.

