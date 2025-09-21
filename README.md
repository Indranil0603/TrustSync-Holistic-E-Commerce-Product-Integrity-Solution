# Meesho Dice Challenge 2025 - data science track

## Overview
This repository contains the code for the Meesho DICE Challenge 2025 - Data Science Track submission. It includes solutions focused on product review enhancement, refund analysis, and seller product verification to address key challenges in the Meesho e-commerce ecosystem.

---

## File Structure

| File/Folder                   | Description                                                        |
|------------------------------|--------------------------------------------------------------------|
| `review-enhancement-pipeline.ipynb`| Pipeline to process and enhance product reviews into feature-specific ratings using embeddings. |
| `etl-pipeline-post-order-analysis.ipynb` | ETL pipeline focused on analyzing delays, refunds and return-related patterns.            |
| `seller-verification-pipeline.ipynb`| Pipeline for verifying seller product images against catalog images using vision models.|
| `customer complain analysis`| Contains code for reddit scrapper and analysis on the reviews|

---

## Technologies and Methodologies

### Review Enhancement Pipeline
- **Data Sources:** Flipkart and Olist product review datasets.
- **Model:** all-mpnet-base-v2 for generating 768-dimensional review embeddings.
- **Methodology:** Semantic similarity and sentiment labeling using cosine similarity with positive and negative sentiment embeddings. User-friendly feature-wise rating calculation via weighted averages.
- **Architecture Diagram:** ![review enhancement pipeline](./images/review-enhancement-pipeline.png)

### ETL Pipeline for Refund Analysis
- **Data Sources:** Amazon US order data (March 2020 – December 2021) for estimating customer/seller statistics and refund patterns.
- **Methodology:** Statistical analysis for identifying sellers with faulty products, customers with high return rates, and zones with delayed deliveries based on order/refund status and delivery timestamps.
- **Architecture Diagram:** ![etl-pipeline-refund](./images/etl-pipeline-refund.png)

### Seller Verification Pipeline
- **Data Sources:** Images from product catalog and seller-uploaded product images.
- **Model:** CLIP Vision Transformer (ViT) to compute similarity scores between catalog and seller images.
- **Methodology:** Products are verified based on similarity scores exceeding a threshold; otherwise flagged for manual check.
- **Architecture Diagram:** ![seller-verification](./images/seller-verification.png)

