# Tweet Analysis of @WeRateDogs
Gathering Data from multiple sources in different file formats to analyze the tweets contained in the archive of WeRateDogs.

### Project Motivation: To extensively wrangle Social Media Data

### Goal: Wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations.

#### The Data: I worked on the following three datasets:
> #### Enhanced Twitter Archive:
> The WeRateDogs Twitter archive contained basic tweet data for all 5000+ of their tweets, but not everything. One column the archive did contain though: each tweet's text, which was used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced." Of the 5000+ tweets, it was filtered for tweets with ratings only (there are 2356). I gathered this data usind the read_csv pandas method.
>
> #### Additional Data via the Twitter API:
> Back to the basic-ness of Twitter archives: retweet count and favorite count were two of the notable column omissions. Fortunately, I was able to gather this additional data by  querying Twitter's API with respect to the tweet ids contained in the archive data. 
>
> #### Image Predictions File:
> The images in the WeRateDogs Twitter archive were ran through a neural network that can classify breeds of dogs. The results: a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images). The file (image_predictions.tsv) containing these detilas was hosted on Udacity's servers. I downloaded  this programmatically using the Requests library.

After gathering the data from these sources, I assesed them individually for quality and tidiness issues. I had a changelog to record all the issues with the data. I Identified 8+ quality issues and 4+ tidiness issues to start with. During the process of cleaning, e.g merging datasets, some further issues came up and I dealt with them immediately

Before cleaning, I made copies of all the three datasets then I started the cleaning process in the recommended order of:
* completeness issues i.e handling null values
* tidiness issues i.e all columns are attributes, all rows are observation and a table is a unit of observation.
* validity issues - whether the data conforms to real world constraints or a defined business constraint
* accuracy issues - whether the data conforms to a standard or true values
* consistency issues - same format for same item across all rows, columns, tables

I majorly used pandas, numpy and regex packages for cleaning. I also used functions like replace() and melt() to metion a few

Finally, after the process of gathering, assessing and cleaning, I asked questions to generate insights and produce univariate and bivariate visualizations.
