# UDA Comment Data and Discussion
*This is a submission for **Lab 2: Web data collection and visualization** in the UW Seattle GEOG 458 course taught by Professor Bo Zhao*

## Background
The Universal Dance Association (UDA) is a major organizer of dance camps, competitions, and more. For this project, we take a look at comments revolving around 2 of the top UDA College Nationals competitors: [**Minnesota Dance**](https://www.minnesotadanceteam.com/) and [**Ohio State Dance**](https://ohiostatebuckeyes.com/sports/2018/7/2/dance-team).

As the popularity of UDA Nationals continues to grow, extending its audience outside of the dance world, the comments made about teams and dancers begins to change. People who have spent their lives in dance are now discussing how increased popularity may shift comments to be more like those seen under NCAA recognized sports. This means an increase in critique and competitiveness among fans, in addition to expected increase in support. While this shift is just beginning, it's important to understand how it affects the overall community, as well as the dancers and teams who are presented for critique.

In order to get a good look at the current commentary, I am looking at Minnesota and Ohio State comments. These two teams have a reputation for being top scorers, specifically in the *Jazz* and *Pom* categories, making their routines some of the most widely viewed and most often discussed. Using data on these teams will *(1)* ensure we have a considerable amount of data, and *(2)* increase the diversity among the pool of commenters. 

## Process
### Data Collection
To collect data, I used a web crawler to extract the comment data on different YouTube videos. In order to make a good comparison, I kept the method as similar as possible, only changing the name of the school in the beginning url and search terms. Here are the specifics:

| | **Minnesota** | **Ohio State** |
| ----- | ----- | -----|
| **URL Source** | [https://www.youtube.com/results?search_query=minnesota+dance](https://www.youtube.com/results?search_query=minnesota+dance) | [https://www.youtube.com/results?search_query=ohio+state+dance](https://www.youtube.com/results?search_query=ohio+state+dance)|
| **Search Terms** | "minnesota", "university of minnesota", "minnesota dance", "minnesota jazz", "minnesota pom", "jazz", "pom" | "ohio state", "ohio state university", "ohio dance", "ohio state dance", "ohio jazz", "ohio state jazz", "ohio state pom", "ohio pom", "jazz", "pom"|


The crawler took all comments and created a csv file for each team. Once inputted into a word cloud generator, I went through all words, removing those that were common or meaningless alone. For example I deleted "wide", "world", and "sports", as they relate to the location in which they compete, and do not add to the comparison. I did choose to leave in names, even though they may not be meaningful without context. I think it is important to see that these comments include specific names. With that being said, this process inherently adds bias, and likely could produce different results if someone else made the deletions. 


### Files
The following are the csv files created by the crawler.

Click to download:
> <a href="assets/minnesota-search.csv" download>minnesota-search.csv</a>

> <a href="assets/ohio-search.csv" download>ohio-search.csv</a>


Header Key: 
- **video_url**: url to the searched video
- **user_url**: url of account that posted the video (this can be added on to the end of "youtube.com/" to find the account)
- **username**: username of the account that posted the video
- **title**: title of the YouTube video
- **view_num**: number of views on the YouTube video
- **created_at**: how long ago the video was posted
- **shortdesc**: the description included in each under the YouTube video, written by the account that posted the video
- **collected_at**: the time in which the data was collected

### Visualizations
**Minnesota**

<img src="img/m-word-cloud.png" alt="maroon and gold words in the shape of a chat bubble" width="500"/>

**Ohio State**

<img src="img/os-word-cloud.png" alt="red, grey, and black words in the shape of a chat bubble" width="500"/>

## Analysis
When looking at the images, there are a good amount of similarities. There are lots of positive descriptors like "champion", "devine", and "talent". You'll also see a lot of first and last names, smaller in the background, though ohio state notably has more. In general I would say that Ohio State not only has more words, but has more large words, indicating them being used more often. This isn't too much of a surprise though as they have won 6 titles in the D1A Jazz category over the last 7 years, making them a very big name in collegiate dance. What did come as a surprise to me was how few times the word "pom" appeared. While the category is smaller and could be less enjoyable for some, I did anticipate that the accounts posting videos would include the word within their descriptions. One reason why this may not have been the case is that the D1A Jazz category has three round of competition, while D1A Pom only has two rounds, which means there is inherently less content containing the pom routines.

I am happy with these results as a starting point, but if I were to do this again I would be interested to see the results of this process done on Instagram or TikTok instead of YouTube. I think that the different platforms are conducive to different types of content and, based on the results, it may be better to get information from a platform known for short-form content. I also think I would want to add in a few of the other top teams that compete in other divisions, that way I can paint a fuller picture of the discourse within the topic.
