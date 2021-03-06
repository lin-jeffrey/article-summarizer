# article-summarizer
In hindsight of the recent 2020 election and the ongoing covid-19 pandemic, there is a constant stream of updating news articles that are hard to constantly keep up with. Especially with a busy schedule, staying well informed during these times is quite difficult and time consuming. My solution for this is to find the most important sentences in an article so that when put together, it can provide the reader a synopsis of the article. 

To do this, I take each sentence in the article and create an tf-idf vector for the sentence, accounting for stopwords and stemming. Then I calculate the cosine similarity between all the sentence vectors in the article to create a similarity matrix. Then using networkx's pagerank function I can then give each sentence a similarity score so that I find the most important sentences in the article. Taking the top 15% of ranked sentences, I can then combine them to form a summary representitive of the full article. 

