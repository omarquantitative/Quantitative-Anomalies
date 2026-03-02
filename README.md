# 🔬 Quantitative Anomalies & Alpha Research

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Research Domain](https://img.shields.io/badge/Domain-Quantitative_Research-blue)
![Data Source](https://img.shields.io/badge/Data-SEC_EDGAR-lightgrey)
![Status](https://img.shields.io/badge/Status-Active_Research-success)

## 📖 Overview
This repository serves as a theoretical research lab and documentation hub for exploitable market inefficiencies. The primary objective is to deconstruct academic papers, structural market inefficiencies, and statistical anomalies, translating them into actionable quantitative edge. 

> **Core Philosophy:** Markets naturally move from inefficiency to efficiency. The concepts documented here represent the temporary, exploitable windows where mispricings occur due to human behavioral biases, liquidity constraints, or asymmetric information processing.

---

## 🏆 Featured Research: Inattentive Pricing (10-K NLP Anomaly)

### 1. The Core Inefficiency: Information Friction
Every year, publicly traded companies file a standardized legal document with the SEC called a 10-K. Because of heavy regulatory burdens and legal review, these documents are largely boilerplate, retaining the exact same formatting, executive language, and risk disclosures year over year. 

However, the market systemically **underreacts** to changes in routine corporate filings due to sheer information overload. In the landmark paper *"Lazy Prices"* (Cohen, Malloy, Nguyen)—referenced here as the Inattentive Pricing anomaly—researchers quantified year-over-year textual similarities using Natural Language Processing (NLP), specifically evaluating Jaccard and Cosine similarity metrics. 



They discovered that when management actively edits the text—especially in the "Risk Factors" or "Management Discussion" sections—it contains highly predictive, alpha-generating information.

### 2. The Strategy & Alpha Generation
* **The Mechanism:** A portfolio that goes long on "non-changers" (companies that duplicate their 10-K from the previous year) and short on "changers" (companies that actively edit their 10-K).
* **The Asymmetry of Sentiment:** The researchers found that **86% of textual changes carry negative sentiment**. Companies face far greater legal liability for failing to disclose negative, material information (lawsuits) than positive information. Therefore, corporate lawyers force management to update the 10-K to mitigate legal downside before negative events are priced into the market.

> **📊 The Edge:** This long/short portfolio earns a statistically significant abnormal return of between **34 and 58 basis points per month**. This compounds to roughly **up to 7% in excess returns (pure alpha) per year**, completely uncorrelated to the broader market.

### 3. Case Study: Baxter International (NYSE: BAX)
For years, the S&P 500 company Baxter International filed almost identical 10-Ks. In their 2009 10-K (released in early 2010), they made unusual, subtle changes to their boilerplate text. The stock traded completely sideways for two months because human investors were largely inattentive to the modifications. 

In April 2010, the FDA cracked down on Baxter's medical IV pumps. The stock plummeted as the market finally priced in the regulatory risk that was quietly sitting in the 10-K the entire time. An NLP algorithm would have detected the textual shift and shorted the asset months prior.

### 4. The Persistence of Edge
This anomaly persisted throughout the entire 20-year period of the academic study. Even though the information was publicly available for free on a government website (SEC EDGAR), the sheer volume of text created an "information friction" that human analysts simply could not process efficiently, leaving the alpha entirely to quantitative algorithms.

---

## ⚙️ Future Implementation Roadmap
To move this from theory to execution, the following infrastructure is being designed for this repository:
- [ ] **EDGAR Scraper:** A Python script utilizing `sec-api` to systematically extract 10-K and 10-Q filings.
- [ ] **NLP Architecture:** Tokenization and text-cleaning logic to strip HTML and boilerplate headers.
- [ ] **Similarity Engine:** Calculating Cosine/Jaccard similarity scores between Year(T) and Year(T-1) filings.
- [ ] **Backtesting Engine:** Mapping similarity scores against historical price data using `yfinance` to verify alpha decay.

---

## 📚 Academic Bibliography & Sources
* **[1]** Cohen, L., Malloy, C., & Nguyen, Q. (2018). *Lazy Prices*. NBER Working Paper No. 25084. 
* **[2]** NBER Digest. (2018). *Are Investors Inattentive to SEC-Mandated Corporate Reports?* (Summary of Working Paper 25084).
* **[3]** U.S. Securities and Exchange Commission (SEC) EDGAR Database (Source of raw filing data).

---

## ⚖️ Disclaimer
**For Educational and Research Purposes Only.** The research and concepts documented in this repository do not constitute financial advice, investment recommendations, or an offer to buy or sell any securities. Trading financial markets involves significant risk of loss. 

## 📄 License
This project is licensed under the **MIT License**.
