# **Live training session name**<br/>by **Instructor**

Live training sessions are designed to mimic the flow of how a real data scientist would address a problem or a task. As such, a session needs to have some “narrative” where learners are achieving stated learning objectives in the form of a real-life data science task or project. For example, a data visualization live session could be around analyzing a dataset and creating a report with a specific business objective in mind _(ex: analyzing and visualizing churn)_, a data cleaning live session could be about preparing a dataset for analysis etc ... 

As part of the 'Live training Spec' process, you will need to complete the following tasks:

Edit this README by filling in the information for steps 1 - 4.

## Step 1: Foundations 

This part of the 'Live training Spec' process is designed to help guide you through session design by having you think through several key questions. Please make sure to delete the examples provided here for you.

### A. What problem(s) will students learn how to solve? (minimum of 5 problems)

> - Understand different ways of performing brand analysis from tweet texts
> - How to compare brand popularity by extracting and comparing follower counts
> - How to promote a brand by identifying popular tweets
> - How to evaluate brand salience and compare the same for two brands using tweet frequencies
> - Understand brand perception through text mining and by visualizing key terms
> - Perform sentiment analysis of tweets to understand customer's feelings and sentiments about the brand
> - Visualize brand presence by plotting tweets on the map


### B. What technologies, packages, or functions will students use? Please be exhaustive.

> - rtweet
> - dplyr
> - reshape
> - ggplot2
> - qdapRegex
> - tm
> - qdap
> - wordcloud
> - RColorBrewer
> - syuzhet
> - maps

### C. What terms or jargon will you define?

_Whether during your opening and closing talk or your live training, you might have to define some terms and jargon to walk students through a problem you’re solving. Intuitive explanations using analogies are encouraged._

> - Time series data: Time series represents a series of data points sequentially indexed over time.  Analyzing time series data helps visualize the frequency of tweets over time.

> - Brand salience: It is the extent to which a brand is spoken about for which volume of tweets posted on the brand is a strong indicator.

> - Corpus: A corpus is a list of text documents and is the starting point for various text processing functions.

> - Sentiment analysis: Sentiment analysis is the process of retrieving information about a consumer's perception of a product or brand. It is used to extract and quantify positive, negative, and neutral opinions as well as emotions like trust, joy, and anger from the text.


### D. What mistakes or misconceptions do you expect? 

_To help minimize the amount of Q&As and make your live training re-usable, list out some mistakes and misconceptions you think students might encounter along the way._

> - Participants might expect to extract live feeds from twitter during the session. We will make it clear that it involves a setup process and the training session will use pre-saved datasets only that contain extracted tweets.


### E. What datasets will you use? 

Live training sessions are designed to walk students through something closer to a real-life data science workflow. Accordingly, the dataset needs to accommodate that user experience. 
As a rule of thumb, your dataset should always answer yes to the following question: 
> Is the dataset/problem I’m working on, something an industry data scientist/analyst could work on? 

Check our [datasets to avoid](https://instructor-support.datacamp.com/en/articles/2360699-datasets-to-avoid) list. 

> -  Tweets on 'tesla' pre-extracted from Twitter
> -  Tweets on 'toyota' pre-extracted from Twitter
> -  Tweets on 'electric car' pre-extracted from Twitter

## Step 2: Who is this session for?

Terms like "beginner" and "expert" mean different things to different people, so we use personas to help instructors clarify a live training's audience. When designing a specific live training, instructors should explain how it will or won't help these people, and what extra skills or prerequisite knowledge they are assuming their students have above and beyond what's included in the persona.

- [ ] Please select the roles and industries that align with your live training. 
- [ ] Include an explanation describing your reasoning and any other relevant information. 

### What roles would this live training be suitable for?

*Check all that apply.*

- [X] Data Consumer
- [X] Leader 
- [X] Data Analyst
- [X] Citizen Data Scientist
- [X] Data Scientist
- [ ] Data Engineer
- [ ] Database Administrator
- [ ] Statistician
- [ ] Machine Learning Scientist
- [X] Programmer
- [ ] Other (please describe)

### What industries would this apply to?

*List one or more industries that the content would be appropriate for.*

> - Retail marketing
> - Customer experience and engagement
> - E-commerce

### What level of expertise should learners have before beginning the live training?

*List three or more examples of skills that you expect learners to have before beginning the live training*

> - Basic knowledge of Twitter and tweets
> - Working knowledge of R
> - Can draw common plot types (barplots) using ggplot and interpret them



## Step 3: Prerequisites

List any prerequisite courses you think your live training could use from. This could be the live session’s companion course or a course you think students should take before the session. Prerequisites act as a guiding principle for your session and will set the topic framework, but you do not have to limit yourself in the live session to the syntax used in the prerequisite courses.

> - Working knowledge of R. The course **Introduction to R** on DataCamp can be considered as a prerequisite


## Step 4: Session Outline

A live training session usually begins with an introductory presentation, followed by the live training itself, and an ending presentation. Your live session is expected to be around 2h30m-3h long (including Q&A) with a hard-limit at 3h30m. You can check out our live training content guidelines [here](_LINK_). 

>
> ### Introduction Slides 
> - Introduction to the webinar and instructor (led by DataCamp TA)
> - Introduction to the topics
>   - Power of social media data
>   - Importance of brand analysis
>   - Why use social media data for brand analysis
>   - Understand different ways of performing brand analysis from tweet texts
>   - Outline the methods that will be covered in live training
>
> ### Live Training
> #### Dataset exploration
> - Load the library `rtweet()` 
> - Explain usage of `search_tweets()` for extracting live tweets (function not to be executed)
> - Import the dataset with extracted tweets using `readRDS()`
> - Check number of rows and columns in the tweet dataframe
> - View the dataframe of tweets
> - **Q&A** 
> #### Compare brand popularity by extracting and comparing follower counts
> - Use `lookup_users()` to collect data on follower counts
> - Under markdown, define: `screen_name`, `followers_count`
> - Extract screen names and follower counts into a dataframe to view results
> #### Promote a brand by identifying popular tweets using retweet counts
> - Extract columns `text` and `retweet_count` from tweet dataframe
> - Sort in descending order of retweet counts using `arrange()`
> - Exclude rows with duplicate text using `unique()`
> - Remove the rownames and view the top 6 unique posts
> - **Q&A**
> #### Evaluate brand salience and compare the same for two brands using tweet frequencies
> - Under markdown, define: time series and brand salience
> - create a time series plot using `ts_plot()`
> - Import extracted tweets of another brand using `readRDS()` and view the tweet dataframe
> - Create time series objects for the two brands using `ts_data()`
> - load the libraries `reshape()` and `ggplot2()`
> - With `merge()`, merge the time series objects with `time` as the common column
> - Stack the tweet frequency columns using `melt()` and view the output
> - Compare brand salience by plotting the frequency of tweets for the two brands using `ggplot()`
> #### Understand brand perception through text mining and by visualizing key terms
> -  **a) Process twitter text**
>   - Import the library library `qdapRegex()`
>   - Extract tweet text from the `text` column in the tweet dataframe
>   - Remove URLs from the tweet text using `rm_twitter_url()`
>   - using `gsub()`, replace special characters, punctuation, & numbers with spaces
> -  **b) Convert processed text to a Corpus**
>   - Under markdown, define: corpus and stopwords
>   - Load the libraries `tm()` and `dplyr()`
>   - Convert processed text to a text corpus using `VectorSource()` and `Corpus()`
>   - Convert the corpus to lowercase with `tm_map()`
>   - Remove English stop words from the corpus using `tm_map()` and `stopwords()`
>   - Using `tm_map()` and `stripWhitespace()`, remove additional spaces from the corpus
> -  **c) Remove custom stop words from Corpus**
>   - Under markdown, define: custom stopwords
>   - Extract term frequencies for top 60 words using `freq_terms()`
>   - Create a vector of custom stop words
>   - Remove custom stop words to create a refined corpus using `tm_map()`
> -  **d) Visualize popular terms in the Corpus**
>   - Visualize the key terms with bar plots created with `ggplot()`
>   - Load libraries `wordcloud()` and `RColorBrewer()`
>   - Create word cloud of popular terms using `wordcloud()`
> - **Q&A**
> #### Perform sentiment analysis of tweets
> -  Load the library `syuzhet()`
> -  Extract sentiment scores using `get_nrc_sentiment()`
> -  Use `colSums()` to calculate sum of sentiment scores
> -  Convert row names into 'sentiment' column and combine with sentiment scores using `cbind()`
> -  Plot and interpret the sentiment scores using `ggplot()`
> #### Visualize brand presence by plotting tweets on the map
> -  Import the extracted tweets on "electric vehicle" using `readRDS()`
> -  Extract geo-coordinates data to append as new columns using `lat_lng()`
> -  Use `na.omit()` to omit rows with missing geo-coordinates in the dataframe
> -  Load the library `maps()`
> -  Using `map()` and `with()` functions, plot longitude and latitude values of tweets on the world map
> - **Q&A**
>
> ### Ending slides
> -  Recap of what we learned
> -  What other brand analysis can be done using the tweets?
> -  Where else can you apply what we learned
> -  Call to action and course recommendations

## Authoring your session

To get yourself started with setting up your live session, follow the steps below:

1. Download and install the "Open in Colabs" extension from [here](https://chrome.google.com/webstore/detail/open-in-colab/iogfkhleblhcpcekbiedikdehleodpjo?hl=en). This will let you take any jupyter notebook you see in a GitHub repository and open it as a **temporary** Colabs link.
2. Upload your dataset(s) to the `data` folder.
3. Upload your images, gifs, or any other assets you want to use in the notebook in the `assets` folder.
4. Check out the notebooks templates in the `notebooks` folder, and keep the template you want for your session while deleting all remaining ones.
5. Preview your desired notebook, press on "Open in Colabs" extension - and start developing your content in colabs _(which will act as the solution code to the session)_.  :warning: **Important** :warning: Your progress will **not** be saved on Google Colabs since it's a temporary link. To save your progress, make sure to press on `File`, `Save a copy in GitHub` and follow remaining prompts. You can also download the notebook locally and develop the content there as long you test out that the syntax works on Colabs as well.
6. Once your notebooks is ready to go, give it the name `session_name_solution.ipynb` create an empty version of the Notebook to be filled out by you and learners during the session, end the file name with `session_name_learners.ipynb`. 
7. Create Colabs links for both sessions and save them in notebooks :tada: 
