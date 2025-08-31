# Fraud-Detection-Capstone
Capstone project on fraud prevention for a U.S. retail rewards app; proposed tiered controls reducing fraud by 26% while keeping 99% user retention.

# Fraud Detection Strategy for Shopkick

**Client: Shopkick with Trax Retail**  

----------------------------------------------------------------------------------------

## Table of Contents  
- [Project Overview](#project-overview)  
- [Background & Problem Statement](#background--problem-statement)  
- [Methodology](#methodology)  
- [Key Findings](#key-findings)  
- [Recommendations & Impact](#recommendations--impact)  
- [Deliverables](#deliverables)  
- [File Structure](#file-structure)  
- [Acknowledgments](#acknowledgments)  

----------------------------------------------------------------------------------------

## Project Overview  
- **Issue**
- Shopkick faces significant fraud issues such as account creation abuse, receipt falsification, and promo code exploitation, causing millions in financial losses annually  
- **Goal**
- Analyze Shopkick's fraud detection system, identify key vulnerabilities, and propose a strategy that prevents fraudulent activities while preserving a positive user experience.  

----------------------------------------------------------------------------------------

## Background & Problem Statement  
- **Shopkick**
- Shopkick is a shopping rewards app where users earn points (called kicks) by: Walking into partner stores, scanning product barcodes, uploading purchase receipts, watching videos or completing offers
- These kicks can be redeemed for gift cards at major retailers
- ![Shopkick Guidance](./Shopkick%20Guidance.png) 
- **Problem Statement**  
- Over $3.5 million losses in 2024 due to fraud, and 90% of losses stem from receipt fraud and promo code abuse, and gaps in verification (no phone/email checks at account creation).  

----------------------------------------------------------------------------------------

## Methodology  
- **Market Research**
- Benchmarked Shopkick vs. Fetch, Ibotta, Rakuten on fraud prevention, payout rules, and verification processes
- For more details, see [Competitor Analysis](./appendix/Strategy%20Canvas.pdf) 
- **Sift Investigation**
- Analyzed Shopkick's fraud detection system and its scoring logic with Shopkick's engineering team, then conduct [SWOT & PEST Analysis](./appendix/SWOT_PEST%20Analysis.pdf) for Shopkick  
- **Fraud Data Analysis**
- Mapped out all fraud types and the potential reason by using Shopkick ourselves, and created [Fraud Map](./appendix/Issue%20Tree.pdf)
- Quantified fraud frequency and losses by type (receipts, promo codes, referrals, scanning, walk-ins, etc.) with data (20000+ transactions and 1000+ users) provided by data analyst
- Note: all the data can't be uploaded due to NDA  
- **Multi-team Interviews**
- Weekly syncs with Engineering, Marketing, and Data teams at Shopkick  
- **Facebook Survey**
- Collected user input on acceptable verification measures and redemption preferences with marketing team

----------------------------------------------------------------------------------------

## Key Findings  
- **Fraud Concentration**  
- Receipt fraud: ~ $2M losses, which means this type of fraudulent activity is our main focus for recommendations  
- Promo code abuse: ~ $340K losses
- Referral code fraud: ~ $120K losses 
- **Fraudster Behavior**  
- Accounts often transact immediately after creation  
- Emails: 87% fraud rate for Hotmail, 79% for Outlook  
- Phone verification delayed >6 days strongly correlated with fraud  
- **Competitor Comparison**    
- Both Fetch and Ibotta require higher redemption minimums and stronger verification such as fingerprint authentication 

----------------------------------------------------------------------------------------

## Recommendations & Impact
- **Recommendations**
- Based on the financial impact of fraudulent activities and the feasibility of implementation, we prioritized all recommendations and then emphasize 5 of them. For details, please see the [Fraud Goal Priority](./appendix/Fraud%20Goal%20Matrix.pdf)
1. **Account Creation Modification**
   Require phone + email verification within 24 hours.  
2. **Tiered Payout Verification**
   Bracketed checks:  
   - $2–25: phone  
   - $50: dual verify (phone + email)  
   - $100: government ID  
   - $500: government ID + phone re-verify  
3. **Workflow Redesign**
   Limit suspicious earning behaviors (rapid scans, repeated receipts)  
4. **Promo Code Prediction**
   Use predictive algorithms to block high-risk promo codes
   For more details, see [Final Report](./Fraud%20Detection%20Report.pdf) 
6. **First Redemption Limit**
   Raise from $2 to $10 to reduce high fraud rates on initial redemptions 
- **Impact of Recommendations (if implemented)**  
- 75% reduction in fraudulent account creation  
- $71K in losses prevented annually via tiered payout verification  
- 49% reduction in promo code fraud  
- 26% reduction in fraudulent users earning rewards

----------------------------------------------------------------------------------------

## Deliverables  
This repository includes:  
- [Final Report](./Fraud%20Detection%20Report.pdf)  
- [Final Presentation Slides](./Final%20Presentation%20Slides.pptx)  
- [Weekly Memos (4 weeks)](./logs/)  
- [Appendix](./appendix/)  

----------------------------------------------------------------------------------------

## File Structure  
- |-Shopkick Guidance.png
- |-logs/
-  --Week 1 Memo.pdf
-  --Week 2 Memo.pdf
-  --Week 3 Memo.pdf
-  --Week 4 Memo.pdf
- |-appendix/
-  --Strategy Canvas.pdf
-  --Issue Tree.pdf
-  --Fraud Goal Matrix.pdf
-  --SWOT_PEST Analysis.pdf
- |-Final Presentation Slides.pptx
- |-Fraud Detection Report.pdf
- |-README.md

---------------------------------------------------------------------------------------

## Acknowledgments   
- **Head of Operations** Richard Froggatt   
- **Director of Marketing** Sarah Jankowski 
- **Engineer Team** AJ Marchese and Marcus Truscello
- **Data Analyst** Chris Gee  

