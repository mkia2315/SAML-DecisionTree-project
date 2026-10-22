Anti-Money Laundering (AML) Project

This project uses a  Decision Tree Classifier  to analyze bank logs and automatically flag suspicious transactions.

What This Project Does:
1.  Balances the Data:  The original data had millions of normal logs but very few fraud logs. The data was down sampled to a perfect 50/50 split so the model could learn fraud patterns accurately.
2.  Builds a Pipeline:  The code automatically turns text data (like currencies and locations) into numbers and feeds them into the Decision Tree.
3.  Keeps it Simple:  The tree is limited to a depth of 3 layers so humans can easily see and explain its exact logic.
4.  Ready for Deployment:  The final model is saved as a .pkl file using joblib so it can be used to run a live fraud-detection API.

The Rules Discovered:
The model automatically flags a transaction as  Laundered  if it hits these three conditions at once:
It is in a specific currency group (like Euros, Dirhams, or Rupees).
The amount is  under $6,114.98  (a classic ML technique of "structuring" used to avoid bank alerts).
It uses highly liquid channels like  Cash Deposits, Cash Withdrawals, or ACH transfers .

---

Acknowledgments
Special thanks to the creators and providers of the SAML-D (Suspicious Anti-Money Laundering Dataset) for making this comprehensive transaction data available to the data science community. Their work enables vital hands-on research into automating financial crime compliance and risk-mitigation modeling.
