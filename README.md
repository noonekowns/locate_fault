# Locating Fault without Comparison to Source File

## Dataset
Our dataset is stored in the dataset folder.

## Evaluation Results
### Overall Effectiveness
Our recommendations are provided in results/recommendations. In summary, even without the source files of buggy versions, DISBL achieved actuary values that are similar to IR-based approaches, and there is sufficient space for improvements.
### Rankings of Real Faulty Files
To figure out to what extent the real faulty files can be localized, we exhibit the rankings of them in the recommendation list in result/rankings. The real faulty files of quite a few bugs get top 5 rankings in the recommendation list, while some other files keep low rankings. Researchers proposed approaches to extract various contents from software engineering documents. If we use such approaches to identify the contents of issue reports, we can further improve the effectiveness of our approach.
