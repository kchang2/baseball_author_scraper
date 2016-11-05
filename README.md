# Baseball Author WebScraper

### Requirements
+ https://addons.mozilla.org/en-US/firefox/addon/places-to-csv/ (to gather history data into CSV file)
+ Pandas, NumPy
+ requests, bs4, collections

### Features
+ Scrapes through each website and pulls tag where author is presented
+ Filters through tags pulled for author name
+ Arranges results in *{(author1, # articles read), (author2, # articles read), ..., (authorN, # articles read)}*

### Complications
+ To scrape each site, you need to pull up the HTML src, so if you don't have internet access, or slow access, it'll really make this program run slower
+ Every HTML site has a different way of formatting, and because their focus isn't entirely on site efficiency, this made scraping really difficult. I spent the majority of the time learning how to successfully extract information. Thus, there may be some duplicate data as I had checked a wide arrange of classes and tags.
+ After scraping the data successfully, there was trouble with extracting the author by automation due to quotations within the string. So, for a number of these sets, I manually went down the list and wrote the authors into a text file. Note that it did not take a long time because I could easily count how many of each instances showed up (same site has same HTML format) in the list of author+html code, so writing the text file was a matter of copy and paste.

Will include nice visualizations later down the road. It is just that categorizing only gives 1D plots or histograms at best, so this visualization is not as important. If needing visuals, would make a swarmplot with legends of authors and the horizontal axis being of which sites.

## Backstory
I was recently asked the following question:
> What one or two baseball writers do you read routinely? 

It may seem like an easy question, but for me I never followed any one particular baseball writer. Sure, I read a lot of articles (both sabremetric and not), but this question made me stop and ponder: **Do I have a favorite author?**. Naturally, my curiosity took this on as a mini project to find out just exactly who I tended to read the most, and if I involuntarily had been reading (preferring) one writer more than another.

## Results
We see that the top 10 authors I read are in this order
+ David Allen, 75 articles
+ Paul Swydan, 10 articles
+ Jeff Sullivan, 9 articles
+ Russell A. Carleton, 9 articles
+ Rob Arthur, 8 articles
+ Dave Cameron, 5 articles
+ David Laurila, 5 articles
+ Chris Cwik, 5 articles
+ Michael Baumann, 4 articles
+ Mark Townsend, 4 articles


### Important Assumptions/Information
+ Note I was really only looking for any sabremetric or studies/insight articles, which is why I filtered out the MLB articles. You can tell from the Jupyter documentation that the MLB dataframe was the largest by far (1000+ vs. 200), and this was after the removal of any Cut4 stories. This is because MLB is my go-to site just for everyday baseball news, and I assumed that most news on there mostly dealt with non-scientific formatted articles. Thus, my assumption was that the articles I read on MLB dealing with STATCAST or any other data-aggregation programs did not make a significant dent to warrant a scraping through this dataset. With 1000+ rows, it would take maybe 1 hr. 
+ There was also a project I was working on this year pertaining to baseball (see https://github.com/kchang2/TP-simperform). This could be the reason why David Allen showed up much more than the other authors. However, after scanning through his articles, it made sense why I chose to select David Allen -- he was a leading person in the field of sabremetrics and baseball data science.
+ Junior Year at Caltech was very busy -- and I had very little time to enjoy baseball, the way I would have liked to. So, it makes sense that the amount of these articles read is small to an everyday reader. I will have you know, an interesting thing I found was during the time of the world series between the Mets and the Royals last year, I had a spike in interest (who wouldn't be giddy? The Royals had a contact/small ball team, and the Mets were sparkling in pitching) and noted that my computer registered hits on NYM vs. KC around 1000+ times (831 for 10/27, 611 for 11/01)! This is likely due to my constant refreshing of the game, but the frequency of it (above Google Play Music @ 761, even the MLB.com site! @ 724) is significant and warrants a citation.�
