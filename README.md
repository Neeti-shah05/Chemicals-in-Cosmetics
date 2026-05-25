# Chemicals-in-Cosmetics

Exploratory data analysis in R on the California Safe Cosmetics Program dataset, which lists cosmetic products containing ingredients known or suspected to cause cancer, birth defects, or reproductive harm. Cleans the data, engineers new features, and produces six visualizations surfacing the most common brands, product types, and chemicals.
What it does

Renames raw PascalCase columns to snake_case and filters out records with no chemical listed
Engineers two new columns: discontinued_flag (Active/Discontinued based on whether a discontinuation date exists) and report_year (integer year extracted from date strings using lubridate::mdy() + year())
Normalizes brand names to Title Case using str_to_title() to merge variants like SEPHORA, Sephora, and sephora before counting
Produces six ggplot2 visualizations: top 10 brands by product count, top 5 product categories and subcategories as pie charts, unique chemicals per product type using n_distinct(), top 10 most common chemicals, and a subcategory drill-down for Titanium dioxide
Exports the cleaned and enriched dataset to NeetiShah_cleaned_cosmetics.csv using write_csv()
