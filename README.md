# Whatsapp Chat Analysys

A Jupyter Notebook with the analysis for a Whatsapp Chat using several techniques of data wrangling, EDA and Sentiment Analysis 



## 🔰 How does it work?
Data is downloaded as a .txt file from Whatsapp App Without Media and loaded in the Jupyer Notebook

### Data Wrangling
- Chat data is organized into three columns:
  - Complete Date
  - User
  - Message
- A **Regex Function** is used for several operations and create a *Message_Modified* column:
  - Lowercase the messages
  - Delete messages with URL
  - Remove numbers
  - Remove messages with spaces
  - Remove special characters
  - Remove repeated letters
- An **Emoji** column is created to identify all the emojis used in messages
- Complete Date information is used to create the following columns.
  - Date [YYYY-MM-DD]
  - Month (Name)
  - Day (Number 1-31)
  - Day (Week Name)
  - Hour
This is what the final dataset looks like:

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/Dataset.png" width = "700">

### Exploratory Data Analysis (EDA)
Several questions were answered using the dataset information.

#### *Who has sent the highest number of messages?*
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/1.png" width = "700">

#### *Messages interactions through time*
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/2.png" width = "700">
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/3.png" width = "700">
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/4.png" width = "700">
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/5.png" width = "700">
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/6.png" width = "700">
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/7.png" width = "700">


#### *Use of Emojis*
*Top Emojis User A*
`[('😘', 7403), ('🥺', 1058), ('😬', 411), ('🤪', 277), ('❤', 266)]`

*Top Emojis User L*
`[('🥺', 1378), ('😘', 1111), ('🥰', 912), ('☺', 622), ('😊', 587)]`

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/8.png" width = "700">


#### *Count of Words*
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/9.png" width = "700">

#### *WordClud*

*Both Users*

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/both.png" width = "300">

*Both Users with Spanish Stop Words*

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/both+sw.png" width = "300">

*A User*

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/A+sw.png" width = "300">

*L User*

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/L+sw.png" width = "300">

### Sentiment Analysis

#### *Spanish Analysis*
Sentiment score {Negative [0 : 0.33] | Neutral [0.33 : 0.66] ! Positive [0.66 : 1]}

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/10.png" width = "700">
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/11.png" width = "700">
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/12.png" width = "700">
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/13.png" width = "700">

*Positive Words*

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/sentiment_spanish_pos.png" width = "300">

*Negative Words*

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/sentiment_spanish_neg.png" width = "300">

*The *Spanish Sentiment Analysis* didn't get good results. Now we want to try to perform a Sentiment Analysis with the Messages Translations to English*

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/translated.png" width = "700">

#### *Sentiment Analysis Using [Text Blob](https://www.analyticsvidhya.com/blog/2021/10/making-natural-language-processing-easy-with-textblob/)*
Sentiment score {Negative [-1 : -0.33] | Neutral [-0.33 : 0.33] ! Positive [0.33 : 1]}

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/14.png" width = "700">
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/15.png" width = "700">
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/16.png" width = "700">
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/17.png" width = "700">

*Positive Words*

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/sentiment_text_blob_pos.png" width = "300">

*Negative Words*

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/sentiment_text_blob_neg.png" width = "300">

#### *Sentiment Analysis Using [NLTK](https://akladyous.medium.com/sentiment-analysis-using-vader-c56bcffe6f24)*
Sentiment score {Negative [0 : -0.05] | Neutral [-0.05 : 0.05] ! Positive [0.05 : 1]}

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/18.png" width = "700">
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/19.png" width = "700">
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/20.png" width = "700">
<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/21.png" width = "700">

*Positive Words*

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/sentiment_NLTK_pos.png" width = "300">

*Negative Words*

<img src = "https://raw.githubusercontent.com/alejo1630/whatsapp_sentiment/main/Images/sentiment_NLTK_neg.png" width = "300">
