# I310D | DATA CURATION AND ANALYSIS OF ANN TOP 200 ANIME

## PROJECT OVERVIEW
For this project, data was extracted from the Anime News Network (ANN) website's "Anime Top 200 Best Rated (bayesian estimate)" page. The BeautifulSoup web scraping API as well as the requests, pandas, and re libraries were used to collect data from the website in a Google Colab Python environment. The pandas dataframe was ultimately converted to a .csv file.

With this project, I aim to provide a dataset that includes information about the top-rated anime, their rankings, user ratings, votes, and format. Ultimately, after finding a large disparity between the maximum and minimum votes, I investigated the correlation between the rating of a given top 200 anime and the amount of votes which determined its rating. More specifically, the question surfaced: is vote count a significant predictor of rating?

#### LINKS
Anime Top 200 Best Rated (bayesian estimate): https://www.animenewsnetwork.com/encyclopedia/ratings-anime.php?top50=best_bayesian&n=200

BeautifulSoup: https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwiZ58iL-eyBAxUEmWoFHXQ2AdcQFnoECBIQAQ&url=https%3A%2F%2Fwww.crummy.com%2Fsoftware%2FBeautifulSoup%2Fbs4%2Fdoc%2F&usg=AOvVaw1CcNi9IVKrGJ31WeQCCb3D&opi=89978449

pandas: https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwjQzpeh-eyBAxWUm2oFHXuaCF4QjBB6BAgMEAE&url=https%3A%2F%2Fpandas.pydata.org%2Fdocs%2F&usg=AOvVaw0XNycME7orfFmvA419K9B2&opi=89978449

## DATA ATTRIBUTES

The dataset consists of the following attributes:

#### Rank
The ranking of the anime based on Bayesian estimation.
  - Data Type: Integer
  - Description: Indicates the position of the anime in the top ratings list.
    
#### Title
The title of the anime.
  - Data Type: String
  - Description: The official title of the anime.
    
#### Rating
The average user rating of the anime.
  - Data Type: Float
  - Description: Represents the average rating given by users.
    
#### Votes
The number of user votes for the anime.
  - Data Type: Integer
  - Description: Indicates the total count of user votes for the anime.
    
#### Format
The format category of the anime (TV, Movie, OAV, or Unknown).
  - Data Type: String
  - Description: Categorizes the anime based on its format, which may be "TV," "Movie," "OAV" (Original Animation Video), or "Unknown" if the format is not clearly specified.

## KNOWN ISSUES/BIASES

#### Data Collection
The data is collected from a specific source, Anime News Network, which may not be fully representative of all anime rating data. Bias could exist due to the source's user demographic or selection of anime titles. Additionally, the range of the votes in the data is extremely large, where some anime's rating were determined by as low as 63 votes.

#### Title Format Determination
The classification of anime format ("TV," "Movie," "OAV," or "Unknown") is based on the presence of specific keywords in the title text. This method may not cover all cases accurately, and some anime formats may be misclassified. For example, there were five instances of "Unknown" anime formats in the dataset.

#### User-Generated Data
The data relies on user-generated ratings and votes, which may be influenced by individual preferences and bias. There is an inherent issue in gathering highly accurate information when polling people who are tied to very strong fanbases. For example, often times voters will vote an enemy franchise very poorly to skew the data and bolster their favorite IPs.

## LICENSE

Copyright 2023 joshhee

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Note: Data collected from the Anime News Network website is publicly available and does not have a specified license. 

