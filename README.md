# X (Twitter) News Bot

A Python-based automated X (Twitter) bot that monitors a Turkish news RSS feed, summarizes recent articles using OpenAI GPT-4o, and posts concise, neutral news tweets on an hourly basis.

## Description

This project is an automated news bot designed to share short, readable summaries of current news. It periodically fetches articles from a Turkish RSS feed, selects one item published within the previous hour, and uses OpenAI GPT-4o to generate a brief, neutral Turkish summary suitable for social media. The bot then formats and posts the result directly to X (Twitter).

The system focuses on timing accuracy, language correctness, and political neutrality rather than engagement optimization.

## How It Works

1. Fetches news items from a predefined RSS feed  
2. Filters articles published in the previous hour (local time)  
3. Randomly selects one eligible news item  
4. Sends the article link (or RSS description fallback) to GPT-4o  
5. Receives a strictly formatted JSON response (title and summary)  
6. Cleans, validates, and formats the content  
7. Posts the tweet automatically via the X API  

## Features

- Hourly automated posting  
- RSS-based news monitoring  
- Turkish language–focused summarization  
- Neutral and non-opinionated output  
- Strict JSON parsing and validation  
- Automatic tweet length control (280 characters)  
- Built-in rate limit handling and retry logic  
- Timezone-aware scheduling (Europe/Istanbul)  

## Technologies Used

- Python  
- OpenAI GPT-4o  
- Tweepy (X API v2)  
- Requests  
- BeautifulSoup  

## Prerequisites

- Python 3.11 or higher  
- OpenAI API access  
- X (Twitter) Developer account with write access  

## Configuration

- RSS source can be changed via `RSS_URL`  
- Posting hours and timing logic can be adjusted in `run_hourly`  
- GPT prompt structure and constraints are fully customizable  
- Tweet format can be modified in the output section  

## Notes

This bot is designed for informational sharing only. It does not reply to users, track engagement metrics, or perform sentiment analysis. Once started, it runs fully autonomously.

## Visual Overview

![Main Panel](PNG/X-BOT_0.png)
![Summary Output](PNG/X-BOT_1.png)
