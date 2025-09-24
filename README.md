# Hybrid Log Classification System

A Python-based log classification system that combines Regex, Sentence Transformers + Logistic Regression, and Large Language Models (LLMs) for accurate log categorization. This hybrid framework efficiently handles predictable, complex, and poorly-labeled log patterns.

## Features

### Regex Classification
- Quickly classifies logs with simple and predictable patterns using predefined rules.
- Sentence Transformer + Logistic Regression
- Handles complex patterns when enough labeled data is available by using embeddings and a logistic regression classifier.
- Large Language Models (LLMs)
- Provides fallback classification for logs with insufficient labeled training data, improving coverage and accuracy.
- FastAPI Integration
- Provides an easy-to-use REST API for uploading log files and receiving classified outputs.

## Architecture

project-root/
- │
- ├── training/            # Code for training models (Regex, Sentence Transformer + Logistic Regression)
- ├── models/              # Saved models (embeddings, logistic regression models)
- ├── resources/           # Test CSVs, output files, images, and other resources
- └── server.py            # FastAPI server

## Example

### Input CSV:

source	log_message
app1	User login failed due to 401
app2	Disk space is running low

### Output CSV:

source	log_message	target_label
app1	User login failed due to 401	Security Alert
app2	Disk space is running low	System Notification

## Author
Yash Taneja
- Master of Science in Business Analytics, University of Texas at Dallas
- [LinkedIn](https://linkedin.com/in/yash-taneja-07) | [GitHub](https://github.com/taneja-yash)
