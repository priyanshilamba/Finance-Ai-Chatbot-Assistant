# AI Financial Assistant Chatbot using Dialogflow

An AI-powered personal finance chatbot built using Google Dialogflow NLP that helps users with:

- Loan Eligibility Checking  
- EMI Calculation  
- Investment Advice  

This project demonstrates the practical application of Artificial Intelligence and Natural Language Processing (NLP) in the FinTech domain.

---

# Project Overview

The chatbot acts as a virtual financial assistant capable of understanding natural language financial queries and providing intelligent responses instantly.

It is designed to solve common financial problems such as:

- Lack of financial literacy
- Complex EMI calculations
- Delayed financial consultation
- Limited banking support hours
- Generic investment advice

The chatbot delivers 24×7 conversational financial guidance using Dialogflow NLP.

---

# Features

## Loan Eligibility Assessment

Checks whether a user is eligible for a loan based on:
- Monthly income
- Requested loan amount
- Safe EMI range

---

## EMI Calculation

Calculates EMI using the standard banking formula:

```math
EMI = P × r × (1 + r)^n / ((1 + r)^n – 1)
```

Where:
- **P** = Principal Loan Amount
- **r** = Monthly Interest Rate
- **n** = Loan Tenure in Months

---

## Investment Advice

Provides investment suggestions based on risk appetite:

| Risk Level | Suggestions |
|---|---|
| LOW | FD, Bonds, Debt Mutual Funds |
| MEDIUM | Index Funds, Balanced Funds |
| HIGH | Equity Mutual Funds, Stocks |

---

## NLP-Powered Conversation

Uses Google Dialogflow for:
- Intent Recognition
- Entity Extraction
- Slot Filling
- Conversational Flow

---

# AI & NLP Concepts Used

## Intent Classification

Maps user queries to financial intents like:
- EMI Calculation
- Loan Eligibility
- Investment Advice

---

## Named Entity Recognition (NER)

Extracts important values such as:
- Income
- Loan Amount
- Interest Rate
- Tenure
- Risk Level

---

## Slot Filling

Automatically asks for missing information during conversation.

---

## Custom Entity

Custom entity used:

```text
risk_level
```

Values:
- LOW → safe, conservative
- MEDIUM → balanced, moderate
- HIGH → risky, aggressive

---

# Dialogflow Architecture

```text
User Query
     ↓
Dialogflow NLP Engine
     ↓
Intent Matching
     ↓
Entity Extraction
     ↓
Parameter Collection
     ↓
Response Generation
     ↓
Financial Recommendation
```

---

# Intents Configured

The following intents were created inside Dialogflow:

```text
Default Welcome Intent
Default Fallback Intent
Loan_Eligibility_Advanced
EMI_Calculation
Investment_Advice_Advanced
Investment Planning
Low Risk Investment
Mutual Fund vs FD
Loan_Request_With_Amount
```

---

# Loan Eligibility Module

## Sample User Queries

```text
I earn 60000, can I get 20 lakh home loan?
Loan eligibility for 60000 income
Can I get loan of 20 lakh?
```

## Parameters Extracted

| Parameter | Type |
|---|---|
| income | @sys.number |
| loan_amount | @sys.number |

## Logic Used

- Uses 30–40% income rule for EMI safety
- Estimates safe EMI range
- Assesses loan feasibility
- Recommends longer tenure when required
- Mentions recommended credit score

---

# EMI Calculation Module

## Sample User Queries

```text
Calculate EMI for 10 lakh at 8% for 5 years
EMI for 20 lakh loan
Calculate monthly installment
```

## Parameters Extracted

| Parameter | Type |
|---|---|
| LOAN_AMOUNT | @sys.number |
| interest | @sys.number |
| tenure | @sys.number |

## Example Calculation

```text
Loan Amount: ₹10,00,000
Interest Rate: 8%
Tenure: 5 Years

Estimated EMI ≈ ₹20,276/month
```

---

# Investment Advice Module

## LOW RISK

- Fixed Deposits
- Government Bonds
- Debt Mutual Funds

Expected Return:
6–7% annually

---

## MEDIUM RISK

- Index Funds
- Balanced Mutual Funds

Expected Return:
10–12% annually

---

## HIGH RISK

- Equity Mutual Funds
- Stock Market Investments

Expected Return:
12–18% annually

---

# Screenshots

## Agent Dashboard

![Agent Dashboard](dialogflow%20ss%201.png)

---

## Loan Eligibility Output

![Loan Eligibility Output](dialogflow%20ss%202.png)

---

## EMI Calculation Output

![EMI Calculation Output](dialogflow%20ss%203.png)

---

# Project Structure

```text
├── Dialogue_Flow.zip
├── README.md
├── intents/
├── entities/
└── screenshots/
```

---

# Setup Instructions

## Step 1: Open Dialogflow Console

Go to:

```text
https://dialogflow.cloud.google.com/
```

---

## Step 2: Create or Open Agent

Create a new Dialogflow agent or open an existing one.

---

## Step 3: Import ZIP File

Navigate to:

```text
Settings → Export and Import → Restore from ZIP
```

Upload:

```text
Dialogue_Flow.zip
```

---

## Step 4: Test the Chatbot

Use queries like:

```text
Can I get a loan for 20 lakh?
Calculate EMI for 10 lakh at 8%
Suggest low risk investments
```

---

# Future Improvements

- Webhook integration for live banking APIs
- Real-time EMI computation
- WhatsApp and Telegram integration
- Multi-language support
- Personalized ML-based financial advice
- Credit score API integration

---

# Technologies Used

- Google Dialogflow
- Natural Language Processing (NLP)
- Intent Classification
- Entity Recognition
- Conversational AI

---

# Use Cases

- Personal finance guidance
- Loan assistance
- EMI estimation
- Investment education
- Banking chatbot automation

---

# Conclusion

This project demonstrates how Dialogflow NLP can be used to build an intelligent financial assistant capable of handling loan-related queries, EMI calculations, and investment guidance through conversational AI.

The chatbot provides instant responses, improves financial accessibility, and showcases the practical implementation of AI in financial services.
