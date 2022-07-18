# Tweet-Analysis-of-WeRateDogs
Gathering Data from Multiple sources in different file formats to analyze the tweets contained in the archive of WeRateDogs.


> Project Motivation
> Context
> Goal: Wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations.
>
> The Data
> I worked on the following three datasets:

> Enhanced Twitter Archive
>
> The WeRateDogs Twitter archive contained basic tweet data for all 5000+ of their tweets, but not everything. One column the archive did contain though: each tweet's text, which was used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced." Of the 5000+ tweets, it was filtered for tweets with ratings only (there are 2356). I gathered this data usind the read_csv pandas method.

> Additional Data via the Twitter API
>
> Back to the basic-ness of Twitter archives: retweet count and favorite count were two of the notable column omissions. Fortunately, I was able to gather this additional data by  querying Twitter's API with respect to the tweet ids contained in the archive data. 

> Image Predictions File
>
> The images in the WeRateDogs Twitter archive were ran through a neural network that can classify breeds of dogs. The results: a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images). The file (image_predictions.tsv) containing these detilas was hosted on Udacity's servers. I downloaded  this programmatically using the Requests library.

> Finally, after the process of gathering, assessing and cleaning, I asked questions to generate insights and produce univariate and bivariate visualizations.
