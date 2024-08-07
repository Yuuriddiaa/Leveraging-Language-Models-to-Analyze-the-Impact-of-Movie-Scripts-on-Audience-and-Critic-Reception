# Leveraging-Language-Models-to-Analyze-the-Impact-of-Movie-Scripts-on-Audience-and-Critic-Reception

## Table of Contents
- [Overview](#overview)
- [Introduction](#introduction)
- [Methodology](#methodology)
- [Dataset Collection](#dataset-collection)
- [Data Processing](#data-processing)
- [Model Training](#model-training)
- [Metrics](#metrics)
- [Results](#results)
- [Discussion](#discussion)
- [How to Use](#how-to-use)

## Overview
This project explores an algorithmic approach to generating and analyzing movie reviews using large language models (LLMs). By utilizing movie subtitles as the primary data source, the project aims to understand how much impact a movie's script has on its audience and critic reception.

## Introduction
This project leverages the power of advanced NLP techniques to generate movie reviews using subtitles. By comparing these generated reviews to human-written ones, the study aims to evaluate the accuracy and relevance of the generated content. The project uses BERT scores for evaluation.

## Methodology
The methodology involves several key steps:

- Data Collection: Scraping subtitles and reviews from various sources.
- Data Processing: Parsing and cleaning the data, summarizing content to fit the token limits of the language models.
- Model Training: Fine-tuning the Llama-3-8b model with the processed data.
- Evaluation: Using BERT scores to evaluate the generated reviews against human-written ones.

## Dataset Collection
The dataset consists of subtitle-review pairs for approximately 8,300 movies from the TMDB list. The data was collected as follows:

- Subtitles: Scraped from Yify Subtitles.
- Reviews: Top 20 reviews for each movie were scraped from IMDb.
- Tools Used: Web scraping was performed using Python APIs like Selenium and Beautiful Soup.
Dataset Collection Code:

#Insert dataset collection code here

## Data Processing
Subtitles
- Parsing: Raw subtitles were parsed to extract scenes based on timestamps.
- Summarization: Scenes were summarized using the BART model to ensure the input tokens did not exceed the 8k token limit of Llama-3-8b.
- Cleaning: Inconsistencies like improper spacing and invalid characters were removed using regular expressions.
Subtitles Processing Code:
#Insert subtitle processing code here

Reviews
- Parsing and Cleaning: Reviews were parsed and cleaned for consistency with the subtitle data. Each subtitle was paired with corresponding reviews, creating around 124,500 training samples (approximately 8,300 movies × 15 reviews per movie).
Reviews Processing Code:
#Insert Reviews processing code here

## Model Training
- Pipeline: Based on Unsloth’s Llama-3-8b fine-tuning notebook.
- Optimization: Used 4-bit quantization for reduced memory usage and QLoRA for efficient fine-tuning.
- Training Setup: Hugging Face’s Supervised Fine Tuning (SFT) trainer was used to configure and perform the training.

Model Training Code:
#Insert training code here

## Metrics
-Metrics like BERT score were used
Evaluation Code:
#Insert evaluation code here

## Results

## Discussion

## How to Use
