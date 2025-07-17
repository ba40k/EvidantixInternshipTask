# Product Name Extraction from Furniture Stores

## Overview
This project provides a solution for extracting product names from furniture store websites using Named Entity Recognition (NER). The system combines web scraping techniques with a fine-tuned BERT model to identify and extract product names from webpage content.

## Solution Architecture

### Key Components
1. **Web Scraper**: Extracts relevant text from furniture store product pages
2. **Custom NER Model**: Fine-tuned BERT model specialized in identifying furniture products
3. **API Layer**: FastAPI-based interface for easy integration
S

## Implementation Details

### Model Training
- **Base Model**: `bert-base-cased`
- **Training Data**: Custom BIO-tagged dataset of furniture product names
- **Labels**: `["O", "B-PRODUCT", "I-PRODUCT"]`
- **Key Metrics**:
  - F1 Score: 0.87
  - Precision: 0.86
  - Recall: 0.88

### Key Features
- **Intelligent Text Extraction**: Focuses on product-relevant page sections
- **Subword Handling**: Special processing for BERT tokenization artifacts
- **Duplicate Removal**: Ensures clean output

## Performance Metrics
Classification Report:
                  precision    recall   f1-score    support

     PRODUCT         0.86       0.88      0.87        48

     micro avg       0.86       0.88      0.87        48
     macro avg       0.86       0.88      0.87        48
     weighted avg    0.86       0.88      0.87        48
- 1771 tokens for training
- 404 tokens for validation

