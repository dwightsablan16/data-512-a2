# DATA 512 ASSIGNMENT 2: BIAS IN DATA
## Background
The goal of this assignment is to explore the concept of bias through data on Wikipedia articles - specifically, articles on political figures from a variety of countries. I will combine a dataset of Wikipedia articles with a dataset of country populations, and use a machine learning service called ORES to estimate the quality of each article. I perform an analysis of how the coverage of politicians on Wikipedia and the quality of articles about politicians varies between countries.

## License

The MIT License is a permissive free software license originating at the Massachusetts Institute of Technology (MIT). As a permissive license, it puts only very limited restriction on reuse and has therefore an excellent license compatibility. For more info please see: [MIT license](https://snyk.io/learn/what-is-mit-license/).

## API and Data
For this assignment we use the ORES [REST API](https://ores.wikimedia.org/v3/#!/scoring/get_v3_scores_context_revid_model)  which provide access to a set of scoring models.

There are two datasets used in this assignment:
Dataset 1: The Wikipedia politicians by country dataset can be found on [Figshare](https://figshare.com/articles/dataset/Untitled_Item/5513449). We download and unzip the data file named page_data.csv.
Dataset 2: The population data is available in CSV format as [WPDS_2020_data.csv](https://docs.google.com/spreadsheets/d/1CFJO2zna2No5KqNm9rPK5PCACoXKzb-nycJFhV689Iw/edit#gid=283125346). This dataset is drawn from the world population data sheet published by the Population Reference Bureau.

## Quality Predictions
In our analysis we're using a machine learning system called ORES. This was originally an acronym for "Objective Revision Evaluation Service" but was simply renamed “ORES”. ORES is a machine learning tool that can provide estimates of Wikipedia article quality. 

The article quality estimates are, from best to worst:
- FA - Featured article
- GA - Good article
- B - B-class article
- C - C-class article
- Start - Start-class article
- Stub - Stub-class article

These were learned based on articles in Wikipedia that were peer-reviewed using the Wikipedia content assessment procedures. These quality classes are a sub-set of quality assessment categories developed by Wikipedia editors. For a given rev_id, ORES will assign one of these 6 categories.

## Project Structure
```
.
├── LICENSE
├── README.md 
├── cleaned_data 
│   ├── no_prediction_data.csv 
│   ├── wp_wpds_countries-no_match.csv 
│   └── wp_wpds_politicians_by_country.csv 
├── hcds-a2-bias.ipynb 
├── src 
│   └── hcds-a2-bias.ipynb 
└── unclean_data 
    ├── WPDS_2020_data.csv 
    └── page_data.csv 
```

