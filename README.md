# Predicting Political Lean of Articles and Analyzing Reader Behaviors Across Austria

## Project Overview
This project aims to predict the political leanings of newspaper articles provided by the Austrian newspaper, derStandard, and analyze the reading behaviors of readers across different regions in Austria. The project utilizes a combination of natural language processing (NLP) techniques, machine learning models, and data analysis methods to achieve its objectives.

## Dataset
The dataset consists of articles from derStandard, an Austrian newspaper. The articles were pre-processed to identify those with political content. The final dataset includes features such as article text, publishing dates, titles, and URLs.

## Methodology
### Data Preprocessing
- The dataset was filtered to include only articles with political content using a pre-defined list of political articles.
- Special HTML characters and tags were removed from the article texts.
- The articles were then parsed from XML format, extracting relevant features such as text, title, and publishing date.

### Political Lean Prediction
- The political lean of each article was predicted using a pre-trained machine learning model (`valurank/distilroberta-mbfc-bias`).
- Articles were translated from German to English using Google Translator API to accommodate the language requirements of the model.
- The model classified articles into various political leans: left, left-center, least-biased, right-center, right, and unknown.

### Data Analysis
- The political leanings of the articles were analyzed along with their distribution across different channels and categories.
- Cross-tabulation was performed to understand the distribution of political leans across different types of content.
- A comprehensive analysis was conducted to explore the reading behaviors of readers across Austria, focusing on their preferences for articles with different political leans.

## Results
- The project successfully classified articles into different political leans, providing insights into the political orientation of content in derStandard.
- The analysis of reading behaviors across Austria highlighted regional differences in political article preferences.
- Visualization techniques were employed to present the distribution of political leans across various channels and categories, offering a clear overview of the political landscape in Austrian media.

## Technologies Used
- **Pandas & NumPy**: Used for data manipulation and analysis.
- **xml.etree.ElementTree**: Utilized for parsing XML data.
- **deep_translator**: Applied for translating content from German to English.
- **Hugging Face's Transformers**: Employed for implementing the pre-trained model for political lean prediction.
- **Matplotlib**: Used for data visualization to present the results and insights.
