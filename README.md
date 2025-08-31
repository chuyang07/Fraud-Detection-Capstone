# Fraud-Detection-Capstone
Capstone project on fraud prevention for a U.S. retail rewards app; proposed tiered controls reducing fraud by 26% while keeping 99% user retention.

# Fraud Detection Strategy for Shopkick

**Johns Hopkins University – Master of Science in Engineering Management (Capstone Project)**  

---

## Table of Contents  

- [Project Overview](#project-overview)  
- [Background & Problem Statement](#background--problem-statement)  
- [Methodology](#methodology)  
- [Key Findings & Impact](#key-findings--impact)  
- [Recommendations](#recommendations)  
- [Deliverables](#deliverables)  
- [File Structure](#file-structure)  
- [Acknowledgments](#acknowledgments)  

---

## Project Overview  

- **Issue**  
  Shopkick faces significant fraud issues such as account creation abuse, receipt falsification, and promo code exploitation, causing millions in financial losses annually.  

- **Goal**  
  Analyze Shopkick’s fraud detection system, identify key vulnerabilities, and propose a strategy that prevents fraudulent activities while preserving a positive user experience.  

---

## Background & Problem Statement  

- **What is Shopkick?**  
  Shopkick is a **shopping rewards app** where users earn points (called *kicks*) by:  
  - Walking into partner stores  
  - Scanning product barcodes  
  - Uploading purchase receipts  
  - Watching videos or completing offers  

  These kicks can be redeemed for **gift cards** at major retailers.  

  *(An illustrative screenshot of the app workflow can be inserted here.)*  

- **Market Context**  
  Shopkick competes with Fetch, Ibotta, and Rakuten in the U.S. shopping rewards market. While it differentiates itself with **real-time pre-purchase rewards** (walk-ins, scans), it lacks robust fraud prevention compared to competitors. :contentReference[oaicite:0]{index=0}

- **Problem Statement**  
  - Over **$3.5 million losses** in 2024 due to fraud.  
  - 90% of losses stem from **receipt fraud** and **promo code abuse**. :contentReference[oaicite:1]{index=1}  
  - Gaps in verification (no phone/email checks at account creation, no tiered payout controls).  

---

## Methodology  

- **Market Research**: Benchmarked Shopkick vs. Fetch, Ibotta, Rakuten on fraud prevention, payout rules, and verification processes. :contentReference[oaicite:2]{index=2}  
- **Sift Investigation**: Analyzed Shopkick’s fraud detection system and its scoring logic.  
- **Fraud Data Analysis**: Quantified fraud frequency and losses by type (receipts, promo codes, referrals, scanning, walk-ins, etc.).  
- **Multi-team Interviews**: Weekly syncs with Engineering, Marketing, and Data teams at Shopkick.  
- **Facebook Survey**: Collected user input on acceptable verification measures and redemption preferences.  

---

## Key Findings & Impact  

- **Fraud Concentration**  
  - Receipt fraud: **$1.76M** losses.  
  - Promo code abuse: **$336K** losses.  
  - Referral code fraud: **$116K** losses. :contentReference[oaicite:3]{index=3}  

- **Fraudster Behavior**  
  - Accounts often transact immediately after creation.  
  - Emails: 87% fraud rate for Hotmail, 79% for Outlook.  
  - Phone verification delayed >6 days strongly correlated with fraud.  

- **Competitor Comparison**  
  - Fetch: uses **Kount** with stronger device fingerprinting.  
  - Ibotta: uses **Imply** with real-time anomaly detection.  
  - Both require higher redemption minimums and stronger verification.  

- **Impact of Recommendations (if implemented)**  
  - 75% reduction in fraudulent account creation.  
  - $71K in losses prevented annually via tiered payout verification.  
  - 49% reduction in promo code fraud.  
  - 26% reduction in fraudulent users earning rewards. :contentReference[oaicite:4]{index=4}  

---

## Recommendations  

1. **Account Creation Modification** – Require **phone + email verification** within 24 hours.  
2. **Tiered Payout Verification** – Bracketed checks:  
   - $2–25: phone  
   - $50: dual verify (phone + email)  
   - $100: government ID  
   - $500: government ID + phone re-verify  
3. **Workflow Redesign** – Limit suspicious earning behaviors (rapid scans, repeated receipts).  
4. **Promo Code Prediction** – Use predictive algorithms to block high-risk promo codes.  
5. **First Redemption Limit** – Raise from $2 to **$10** to reduce high fraud rates on initial redemptions.  

---

## Deliverables  
This repository includes:  
- [Fraud Detection Report](./Fraud%20Detection%20Report.pdf)  
- [Final Presentation Slides](./Final%20Presentation%20Slides.pptx)  
- [Weekly Memos (4 weeks)](./logs/)  
- [Appendix (Issue Tree, Strategy Canvas, SWOT/PEST, Goal Matrix)](./appendix/)  

---

## File Structure  

