# Overview

During the Capitol storming on January 6, 2021, what kinds of sentiment manifested in the English tweets discussing U.S. electoral affairs? I conduct sentiment analysis with 270,000 Tweets. This exercise was an assignment for the course session [Supervised Sentiment Analysis in R](https://github.com/ccs-amsterdam/r-course-material/blob/master/tutorials/sentiment_analysis.md) by [@ccs-amsterdam](https://github.com/ccs-amsterdam).

# Data Availability and Provenance Statements

My assignment uses the data from [2020 US Presidential Election Tweet IDs](https://github.com/echen102/us-pres-elections-2020#2020-us-presidential-election-tweet-ids) collected by [@echen102](https://github.com/echen102) and [@emilioferrara](https://github.com/emilioferrara). The following conditions apply:

> This dataset is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International Public License (CC BY-NC-SA 4.0). By using this dataset, you agree to abide by the stipulations in the license, remain in compliance with Twitter’s Terms of Service, and cite the following manuscript:
> 
> Chen, E., Deb, A. & Ferrara, E. #Election2020: the first public Twitter dataset on the 2020 US Presidential election. J Comput Soc Sc (2021). https://doi.org/10.1007/s42001-021-00117-9

Specifically, Twitter's Terms of Service only allows the sharing of Tweet IDs. To retrieve the original text based on Tweet IDs (or to "hydrate"), you need to access the Twitter API yourself. A suitable tool with GUI is [Hydrator](https://github.com/DocNow/hydrator).

## Statement about Rights

I certify that I have legitimate access to and permission to use the data. 

## Summary of Availability

Some data cannot be made publicly available.

## Dataset list

| Data files  | Source | Notes               | Provided |
| ----------------- | ------ | ------------------- | -------- |
| `ElecTweetID.csv` | [us-pres-elections-2020](https://github.com/echen102/us-pres-elections-2020#2020-us-presidential-election-tweet-ids)  | Tweet IDs for retrieving original Tweets | Yes |
| `Capitol_tweet_0106.csv` | Twitter API |  | No |

# Computational requirements

I adopt `R` (version 4.2.0) for all the analyses. This involves the following packages:
`quanteda` (3.2.0), `quanteda.textplots` (0.94.1), `quanteda.textstats` (0.95), `readr` (2.1.2), `syuzhet` (1.0.6)

## Memory and Runtime 

Less than ten minutes is needed to reproduce the analyses on a standard 2022 desktop machine. This does not account for Chunk 37, which takes a long time to run. The code was last run on a Windows 11 laptop with a 4-core Intel processor. 

# Instructions to Replicators

Download `ElecTweetID.csv`. Load it in Hydrator to access Twitter API and retrieve the original text. Save the collected tweets as `Capitol_tweet_0106.csv`. Place it and `script.Rmd` in the same folder. Run the script to execute all steps in sequence. Chunk 37's execution is time-consuming; Skip it if necessary.

The script is provided in the same folder. Run `script_tweet_sentiment.Rmd` to execute all steps in sequence. 

# Reference

Chen, E., Deb, A., & Ferrara, E. (2021). #ELECTION2020: The first public twitter dataset on the 2020 US presidential election. *Journal of Computational Social Science, 5*(1), 1–18. https://doi.org/10.1007/s42001-021-00117-9 
