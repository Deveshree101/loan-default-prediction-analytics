# Detailed Context

## Overview

This page expands on the reasoning, research, and context behind the project. It’s written for readers who want to understand the motivation, assumptions, and deeper thinking that guided each step.

## Problem Understanding

This project simulates a risk-scoring model for micro-lenders serving blue-collar and low-income borrowers. It is inspired by joint-liability and group-lending practices used by MFIs(Micro-Finance Institutions) such as Arohan Financial Services, Spandana Sphoorty and Kosh, and by the Grameen model more broadly (for background). 

These companies are focused on providing access to affordable credit for the informal workforce. I named the company ‘**GramBond**’ for this project. The company provides loans to low-wage/blue -collar workers through an app. Low-wage workers often lack a formal credit history or traditional collateral. GramBond operates on a **Joint Liability Group (JLG) model**, where small groups of borrowers (typically 4–10 individuals) take loans together and share collective responsibility for repayment. The JLG model functions as a system of **social collateral**: each member’s trust and reputation act as the guarantee for the others. Every member receives an individual loan, but if one person defaults, the rest of the group must step in to cover the payment. This shared accountability significantly lowers the lender’s credit risk, especially for borrowers who don’t have a formal CIBIL score or collateral.

There are certain challenges that **GramBond** faces that makes it difficult to predict accurately whether the customer will default on the given loan or not. Some of them are listed below-**:**

- **Limited Credit Data:** Traditional credit scores or histories are often unavailable.
- **Operational Risk:** Defaults, especially group defaults, can have a cascading effect on loan portfolios.
- **Funding Constraints:** Many startups depend on partnerships with NBFCs (Non-Banking Financial Company) or banks for lending capital; repayment issues can strain these relationships.
- **Diverse Borrower Demographics:** Borrowers vary widely in income, employment type, and financial literacy, requiring nuanced lending strategies.
- **Market Education:** Many borrowers are new to digital lending platforms, making onboarding and trust-building important.

All these factors makes it important for company ‘X’ to predict the risk profile for a customer before lending them loan. Also, if the credit history of the customer is unavailable , then it is important to make full use of data and make informed decisions.
[Return to main page](README.md)
