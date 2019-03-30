# FinalProjectDataMining
{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Lobste.rs User Engagement Project"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "This code looks into the site data for Lobste.rs and adds the features of engagement score and comment sentiment to better get an idea of the users who are most active and produce the most engagement and positivity on a whole. They will be combined with survey data to create profiles on certain types of users on the Lobste.rs site."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# FEATURES"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Part 1: Create the engagement score\n",
    "\n",
    "The engagement score metric is a combination of all major actions that a user can take in response to a post. We chose to include all responses, negative and positive, in order to identify those that will bring the most users that are more likely to respond to calls to action placed by marketers on the site"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "1. Load the dataframe (df) using pandas read (pd.read)\n",
    "2. Add the engagement score column by creating a df for engagement score that equates to the upvotes, downvotes and comment count added up.\n",
    "3. Save the original dataframe so you have that separate from the engagement score dataframe\n",
    "4. Drop the columns without comments so that we can analyze only the posts with comments\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Part 2: Calculating Comment Sentiment\n",
    "We decided to use comment sentiment score as our other feature to determine the users who create positive discussion on the site, something that is more valuable in the eyes of advertising firms. These two features can and most likely will overlap in some users, resulting in those that will be most profitable to cultivate and study closer.\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "1. The first function we create uses clean and text_nt to clean the HTML tags from the string\n",
    "2. The second function takes the URL and returns the sentiment score and text of the post comments. Beautiful Soup finds all of the comments, the function we created in step 1 drops the HTML tags, and sentiment score is determined using Vader. Vader uses a list of words which are labeled as positive or negative based on their semantic origin.  \n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Part 3: Finding the Whales and Statistical Test\n",
    "We now determine the top users, or whales,  by examining engagement score and comment sentiment. Then, we calculate the standard deviation and mean of these metrics. \n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "1. Highlight the whales by creating a total engagement score by username by grouping the username with the engagement score.\n",
    "2. Group by comment sentiment to show users who produce the most positive comments on the site\n",
    "3. Count the total posts by each username and drop those who have not posted often\n",
    "4. Find the average post engagement per username and if they have posted more than ten times\n",
    "5. Find the average comment sentiment per post per username if they have posted ten or more times.\n",
    "6. Calculate the standard deviation of engagement score and of comment sentiment\n",
    "7. Calculate the mean of engagement score and comment sentiment\n",
    "8. Find engagement score and comment sentiment standard deviation levels\n",
    "9. Calculate the correlation between engagement score and comment sentiment.\n",
    "\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Part 4: User Data Drill Down\n",
    "Examining our metrics - engagement score, comment sentiment, number of posts and average post engagement  - per username allows us to drill down on our whales’ profiles. \n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "1. Find the total engagement score, total comment sentiment, number of posts and average post engagement per username (separately). \n",
    "2. Determine average post sentiment per user\n",
    "3. Calculate the users at different standard deviation levels from the average post engagement score mean\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Part 5: Visualizations\n",
    "These visualizations give us good insight into the makeup of the users and the those that produce the most popular posts. You can see how there is a small section of targeted users that make up most of the posting and have the highest sentiment scores.\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "1. Plot a histogram of engagement score for all posts\n",
    "2. Plot a histogram of total comment sentiment by username\n",
    "3. Plot a histogram of total engagement score by username\n",
    "4. Plot a histogram of the total posts by username\n",
    "5. Plot a histogram of the average post engagement score by username\n",
    "6. Plot a histogram of the average post comment sentiment by username\n",
    "7. Plot a histogram of the average post engagement scores with different standard deviation levels \n",
    "8. Plot a histogram of the average post comment sentiment with different standard deviation levels \n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# INSTALLATION"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "\n",
    "Install the project by running python, pandas, numpy, statistics, requests, csv, re, nltk, time, warnings, html from lxml, BeautifulSoup from bs4 and SentimentIntensityAnalyzer from nltk.sentiment.vader\n",
    "\n",
    "You will also need the dataset, which is private. \n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Sources\n",
    "----------\n",
    "-Lobste.rs site: https://lobste.rs/\n",
    "\n",
    "- Issue Tracker: https://gitlab.com/haleydeleon/uf-data-analytics-project/issues\n",
    "- Source Code Draft 1: https://github.com/samauer14/FinalProjectDataMining/blob/master/Final%2BProject%2B-%2BAnna.ipynb"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.6.5"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
