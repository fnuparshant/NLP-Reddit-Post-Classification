# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) **Project 3: Web APIs & NLP**
### Executive Summary
**Do you want to elevate your business?** Yes, you are about to achieve that. It is simple; you should understand the market trends and customer's interests. The growth of the organization depends on customer's trust in the company and how well the company understands its customers.

The challenge is how to know the trends and customer's interests. It is so important to stay up to date with trending topics and upcoming events related to your products; else, you will face losses by selling products in which customers have least or no interest, which gives an advantage to your competitors.

**Calm Down!** There is always a solution. The best way to know the trends is through social media. As a company that sells Chess and Football products, you should be aware of things going on in social media under these topics and hashtags. When events like the **Euro Cup** or **FIFA World Cup** are happening, you should sell Football products related to the trend. It can be achieved using Natural Language Processing (NLP) which understands, analyzes, and interprets human language. Our product scrapes the recent content from social media. The social media data is processed with NLP and classified into two categories, i.e., "Chess" and "Football," with the help of the Naive Bayes classifier, which performs with more than 90% accuracy.

Now you are up to date with the topics and events happening related to Chess and Football to sell the most relevant products that interest the customers and What? It is a profit!!

We love to collaborate with an esteemed organization like yours. We will help you to get the best for your customers.

**The Best We Give For Our Customer, The Best We Get For Us!**

## Problem Statement

- Predicting if a post came from Chess or Football subreddit.
- The goal of this project is to help companies that sell chess and football products make more money.

 [![Screen-Shot-2021-07-27-at-4-48-06-PM.png](https://i.postimg.cc/PxmMWvvG/Screen-Shot-2021-07-27-at-4-48-06-PM.png)](https://postimg.cc/Hck5Hxt3) [![Screen-Shot-2021-07-27-at-4-48-17-PM.png](https://i.postimg.cc/sxm98FJw/Screen-Shot-2021-07-27-at-4-48-17-PM.png)](https://postimg.cc/Lgq1Ybw1)


### **My Approach:**
I scrapped recent 5000 posts each from **[Football subreddit](https://www.reddit.com/r/football/)** and **[Chess subreddit](https://www.reddit.com/r/chess/).** I converted them into a **[dataframe](https://www.tutorialspoint.com/python_pandas/python_pandas_dataframe.htm)** and then cleaned and preprocessed it. Then I used **[CountVectorizer](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.CountVectorizer.html)** to get the top 50 words used in post titles of all the 5000 football and 5000 chess posts. At the end I trained **[Random Forest](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html), [Logistic regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html),** and **[Naive Bayes](https://www.datacamp.com/community/tutorials/naive-bayes-scikit-learn)** models to predict whether a post came from Chess or Football subreddit.


### **Findings:**
- Some of the top words that were in post titles of Chess subreddit were : **Fide** (International Chess Fed.), **Pawn** (8-Black & 8-White, **Tournament**, **Elo** (Player rating system), **Board**, **World Championship**, **Queen** : Most powerful, **LiChess** : Free online chess server.
- Some of the top words that were in post titles of Football subreddit were : **Premier Leagues**, **Copa America Tournament** : This year happened in Brazil and Argentina won it, **UEFA Euros Cup** : Last year happened in England and Italy won it, **Real Madrid Club**, **Manchester United Club**, **Chelsea Football Club**, **Messi**, and **Ronaldo.**
### Conclusions And Recommendations :
- Companies selling Chess and Football products can also be benefited with our findings. We can let them know the top 25-50 words (some of them are mentioned above in the findings)  that appeared in the titles so that they can focus on them and make more products related to them to make money.
- I have compared all the models on the basis of their score and Accuracy. I have chose accuracy and not specificity because here we are not worried if we have some false positives (like I predicted that a post came from Chess but it was actually from Football, it is not doing any harm to anyone). Here we are just trying to get our predictions right as much as possible.
- All the three models (RF, Logistic, and Naive Bayes) performed really well as all of them have cross_val_score and accuracy more than 90.
- Naive Bayes model was the best among them with an accuracy of 93.7%, which is way better than our baseline score (52%). This means that our model will correctly predict 94 out of 100 times that a given post came from Chess or not.
