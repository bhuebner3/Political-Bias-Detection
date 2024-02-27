# Predicting Political Lean of Articles and Analyzing Reader Behaviors Across Austria

## Project Overview
This project was performed in partnership with the Austrian newspaper, derStandard, and therefore the data is not publicly available. The project aimed to predict the political leanings of newspaper articles provided by derStandard, and analyze the reading behaviors of readers across different regions in Austria. To achieve these objectives, a combination of natural language processing (NLP) techniques, machine learning models, and data analysis methods are used.

## Technologies Used
- **Pandas & NumPy**: Used for data manipulation and analysis.
- **xml.etree.ElementTree**: Utilized for parsing XML data.
- **deep_translator**: Applied for translating content from German to English.
- **Hugging Face's Transformers**: Employed for implementing the pre-trained model for political lean prediction.
- **Matplotlib**: Used for data visualization to present the results and insights.

## Methodology
### Data Preprocessing
- The dataset was filtered by article category to include only articles with possible political content.
- Special HTML characters and tags were removed from the article texts.
- The articles were then parsed from XML format, extracting relevant features such as text, title, and publishing date.
- User location was assigned based on the users most frequently occuring location.

This plot displays the location where users are accessing articles on the derStandard website. Note: as expected, the largest cities (Vienna, Linz, Graz, etc.) contain the largest share of clicks.

![austria_map](https://github.com/bhuebner3/Political-Bias-Detection/assets/73898316/2655b54c-f131-4bc7-8560-40520e95dcad)



### Political Lean Prediction
- The political lean of each article was predicted using a pre-trained machine learning model (`valurank/distilroberta-mbfc-bias`).
- Articles were translated from German to English using Google Translator API to accommodate the language requirements of the model.
- The model classified articles into various political leans: left, left-center, least-biased, right-center, right, and unknown.

### Data Analysis
- The political leanings of the articles were analyzed along with their distribution across different channels and categories.
- Cross-tabulation was performed to understand the distribution of political leans across different types of content.
- A comprehensive analysis was conducted to explore the reading behaviors of readers across Austria, focusing on their preferences for articles with different political leans.

The following plot shows the predicted political lean by category. Note: blue and red indicate right and left leaning, respectively, as is represented in Austrian politics.

![pol_lean_category](https://github.com/bhuebner3/Political-Bias-Detection/assets/73898316/5381cc25-7af8-4068-a8e7-f099d5b10f84)

The next plot shows the political lean of articles read at different locations in Austria. Although the locations do not show a clear connection with political lean, this may be a result of how the location data is collected, the translation to English affecting the predictions, or other possibilities.

![pol_lean_city](https://github.com/bhuebner3/Political-Bias-Detection/assets/73898316/b358d295-cdc6-4763-9fd8-6e7c99e29a61)



## Results
- The project successfully classified articles into different political leans, providing insights into the political orientation of content in derStandard.
- The analysis of reading behaviors across Austria highlighted regional differences in political article preferences.
- Visualization techniques were employed to present the distribution of political leans across various channels and categories, offering a clear overview of the political landscape in Austrian media.
