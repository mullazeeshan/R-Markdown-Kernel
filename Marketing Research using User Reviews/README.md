# Market Research Using User Reviews
### Goal: To select attributes for marketing of products from online reviews for various brands and analyse the market.</br>
· Collected reviews of products from website by web scraping.</br>
· Reviews were clustered together to get a cluster representing an attribute.</br>
· Correspondence analysis was done using attributes and brands to make a perceptual map of market.</br>

Contents :
1 . Introduction
2. Approach
3. Dataset description
4. Methodology
5. Evaluation
6. References

# Central to marketing
● Key step in
○ Design and development of new products
○ Repositioning of existing products

● Describes substitution and complementary relationship between brands
● Predicts market responses to:
○ Changes in pricing
○ Market strategy
○ Product introduction

# Traditional Approach to Market Structure Analysis
● Uses Surveys
● Uses the thought:
○ “All customers perceive all products the same way with difference in attribute evaluation only”
● Little research on how to choose product attributes i.e. keywords
● Voice of Customer not being used for choosing keywords for marketing 


# Our Approach ● Data Collection:
○ Web Page scraping to get user reviews

● Clustering:
○ Term-Document Matrix
○ Clustering of terms based on cosine similarity
○ Using k-means
● Correspondence Analysis
Data Collection : We collected the online user reviews for digital cameras

# Scraping
Web scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort.

![snip-dp](https://user-images.githubusercontent.com/29397302/85880976-83d98880-b7fa-11ea-9f9e-51e6501e10e8.JPG)

## Beautiful soup
It is a python library for pulling out data from Html and xml files
● Beautiful soup parses the document using the best available parser . (we have used html parser).
● Beautiful Soup transforms a complex HTML document into a complex tree of Python objects.
## Identifying the useful
links :
● Fetch all tags <a href=’...’ >
● Use regular expressions to extract links of products.

## Extract reviews :
● Iterate over all the links we got .
● Find all elements <div class = ‘message >
● Iterate over all div tags and fetch <p>...<p>


# Data Preprocessing
1. Convert in lowercase
2. Remove stopword
3. Remove punctuation
4. Remove url
5. Stemming

# K-means Clustering
It is partition based algorithm. It is most popular algorithms for text mining. It is efficient on the large data. It work on the numerical data.

# Elbow Method
It is used to choose optimal no of cluster.This method cannot give you the optimal number of clusters as an exact point, it can give you an optimal range.


# Correspondence Analysis
● Multivariate statistical technique
● Geometric approach to categorical data analysis
● Deals with categorical data
● Perceptual maps are plotted for extracted components

# Correspondence Analysis process
![contigency](https://user-images.githubusercontent.com/29397302/85880173-33adf680-b7f9-11ea-9a44-b5c8501df164.JPG)
Contingency table
Tasks:
● Relationship between Attributes

● Relationship between Brands

● Relationship between Attribute and Brands

● Representing these relationships in a low dimensional space

# Perceptual Map
Implemented using #FactoMineR and #factoextra in R

![imgg1](https://user-images.githubusercontent.com/29397302/85881195-dca92100-b7fa-11ea-947f-8f07141bb6f9.JPG)

# Scree plot

![imgg2](https://user-images.githubusercontent.com/29397302/85881201-e03ca800-b7fa-11ea-9bc2-c76cc9c8972e.JPG)


