# Comparative Analysis of Sponsored vs. Organic Content on Fitness TikTok

> **Does selling out mean selling short?**

A data-driven analysis of 2,500 TikTok videos to quantify the impact of sponsorship on linguistic authenticity and viewer engagement.

## Project Overview

Influencer marketing is projected to reach **$32.55 billion by 2025**, with TikTok emerging as a dominant platform. 

However, a key question remains: *Does the commercial nature of sponsored content degrade the authenticity that drives engagement?*

This project analyzes the "Sell-Out Effect" in the fitness niche. By scraping and analyzing 2,500 videos from 25 creators, we developed a custom **Authenticity Index** and employed a **Multi-Agent AI Architecture** to determine how sponsorship alters linguistic patterns and how audiences react to those changes.

## Key Features & Methodology

### 1\. Data Collection Pipeline

  * **Source:** TikTok (Fitness Niche).
  * **Sample:** 25 Creators stratified by follower count (Low: \<100k, Medium: 100k-1M, High: \>1M).
  * **Volume:** 2,500 Videos analyzed.
  * **Tools:** Python, `yt-dlp` for scraping video metadata and transcripts.

### 2\. The "Authenticity Index" Algorithm

We engineered a custom composite score (0-100) to quantify how "real" a video sounds using NLP.

$$
\text{Authenticity Score} = \sum(\text{Warmth}, \text{1st Person}, \text{Readability}) - (\text{Commercial Intent})
$$

  * **VADER:** Used to measure emotional valence (sentiment intensity).
  * **Empath:** Used to analyze topics.
      * *Positive Signals:* Warmth (family, friends, trust), Immediacy ("I", "me", "my").
      * *Negative Signals:* Commercialism (money, business, selling terms).

### 3\. Multi-Agent AI Architecture

To deepen the analysis, we deployed a Multi-Agent system using **Gemini-2.5-flash** to categorize content strategy:

  * **Content Effectiveness Agent:** Analyzes hooks and content structure.
  * **Audience Response Agent:** Evaluates emotional triggers and value delivery.
  * **Brand Strategy Agent:** Determines positioning and strategic objectives.

-----

## Key Findings

### 1\. The "Sell-Out" Effect is Real

There is a statistically significant drop in linguistic authenticity when a video is sponsored ($p<0.001$).

  * **Organic Content Mean Score:** 42.35
  * **Sponsored Content Mean Score:** 36.72.

### 2\. The "Mega-Influencer" Paradox

The bigger the influencer, the "faker" they sound in ads.

  * **High Tier (\>1M followers):** Authenticity drops by **10 points** in sponsored videos.
  * **Low Tier (\<100k followers):** Authenticity drops by only **1.6 points**.

### 3\. Authenticity Pays (Literally)

Even within sponsored content, "sounding human" correlates with success. Authenticity is a positive predictor of Engagement Rate ($p<0.001$). Videos that maintained warmth and first-person language performed significantly better than scripted, commercial-heavy videos.

### 4\. Emotional Triggers

Deep emotional triggers (content focusing on feelings/experiences) generated **23.3% higher engagement** than shallow emotional triggers.

-----

## Tech Stack

  * **Language:** Python
  * **Data Collection:** `yt-dlp`
  * **NLP & Sentiment Analysis:** VADER, Empath
  * **AI Models:** Gemini-2.5-flash (via API)
  * **Statistical Analysis:** Mixed Linear Models (MLM), T-tests
  * **Visualization:** Matplotlib, Seaborn

-----

## Recommendations

Based on the data, we propose the following strategies for the industry:

| Stakeholder | Recommendation |
| :--- | :--- |
| **For Brands** | **Stop forcing scripts.** High-authenticity ads perform better. Allow creators to use their natural voice and monitor their "Authenticity Score" during selection. |
| **For Creators** | **Maintain the "I/Me" connection.** Even in ads, use first-person pronouns and focus on personal stories to mitigate the engagement drop-off. |

-----

## Repository Structure

```bash
├── data/               # Anonymized dataset samples
├── code/               # Python scripts for NLP and Statistical Analysis
├── report/             # PDF report covering the causal research strategy
└── presentation/       # PDF of the final findings
```

## Contact

**Author:** Vibhuti Gandhi

**Course:** BUS 439 Analytics Project (Fall 2025)

**Email:** vga17@sfu.ca

-----

*Citations reference the project presentation "Comparative Analysis of Sponsored and Organic Content on Fitness TikTok".*
