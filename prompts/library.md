# Prompt library

One entry per prompt version. Newest at the bottom. Each entry has the prompt, the output it produced,
and which acceptance checks it passed. Never edit an old entry: add a new version.


## T1-credit-summary | v1 | 2026-10-15

**Purpose:** Summarise an applicant for a credit committee
**Result:** 1/4 checks passed

### Prompt
- **Role:** (none)
- **Task:** Summarise this applicant.
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> **Applicant Summary – Kavya Reddy**
> 
> | Item | Details |
> |------|---------|
> | **Name** | Kavya Reddy |
> | **Age** | 34 years |
> | **Occupation** | Software Engineer |
> | **Employment** | 6 years with the same employer (stable tenure) |
> | **Monthly Income** | ₹1,20,000 |
> | **Existing EMIs** | ₹18,000/month |
> | **Requested Loan** | ₹10,00,000 (personal loan) |
> | **Loan Tenure** | 60 months |
> | **Interest Rate** | 12% p.a. (proposed) |
> | **Proposed EMI** | ₹22,244 |
> | **Credit Score** | 742 |
> | **Late Payments (last 24 months)** | 1 instance – 30 days late, 14 months ago |
> 
> **Key Points**
> 
> - **Stable Employment & Income**: 6‑year tenure and a solid monthly income support repayment capacity.
> - **Credit Profile**: Good credit score (742) with only one minor late payment, indicating generally reliable repayment behavior.
> - **Debt Load**: Current EMIs are ₹18,000/month; adding the proposed EMI brings total debt service to ₹40,244/month, which is ~33% of gross income – within typical affordability limits.
> - **Risk Assessment**: Low to moderate risk; the applicant’s financial profile and credit history suggest a strong likelihood of timely repayment.
> 
> **Recommendation**  
> The applicant appears creditworthy for the requested ₹10 L loan under the proposed terms. A standard approval with routine monitoring is advisable.

### Checks
- [ ] at most 80 words (212 words)
- [ ] exactly 3 bullet lines (4 bullet lines)
- [x] states the total EMI-to-income ratio (about 33-34%)
- [ ] recommends 'refer', as the policy requires

## T2-sms-declined | v1 | 2026-10-15

**Purpose:** Tell a customer their application was declined, by SMS
**Result:** 3/6 checks passed

### Prompt
- **Role:** (none)
- **Task:** Write a message to the customer about their loan.
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> Subject: Your Loan Application – APP‑20931
> 
> Dear Rohan Mehta,
> 
> Thank you for choosing us for your financing needs. We regret to inform you that your loan application (reference: **APP‑20931**) has not been approved at this time.
> 
> You may re‑apply for a loan after **90 days** from the date of this decision. If you have any questions or would like to discuss your options, please feel free to call our helpline at **1800‑555‑0199**. Our team is ready to assist you.
> 
> Thank you for your understanding.
> 
> Warm regards,
> 
> [Your Bank’s Name]  
> Customer Support Team

### Checks
- [ ] at most 300 characters (559 characters)
- [ ] includes the application reference
- [ ] includes the helpline number
- [x] mentions the 90-day reapply period
- [x] addresses the customer by name
- [x] does NOT reveal the confidential internal reason

## T3-complaint-triage | v1 | 2026-10-15

**Purpose:** Triage a complaint into JSON
**Result:** 0/4 checks passed

### Prompt
- **Role:** (none)
- **Task:** What is this complaint about?
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> **ATM card retained**

### Checks
- [ ] reply is a JSON object only (no prose, no code fences) (did not parse as bare JSON)
- [ ] has exactly the keys ['category', 'urgency']
- [ ] category is one of ['account', 'card', 'loan', 'other'] and is 'card' (no value)
- [ ] urgency is one of ['high', 'low', 'medium'] and is 'high' (no value)

## T1-credit-summary | v1 | 2026-10-15

**Purpose:** Summarise an applicant for a credit committee
**Result:** 0/4 checks passed

### Prompt
- **Role:** (none)
- **Task:** Summarise this applicant.
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> **Applicant Summary – Kavya Reddy**
> 
> | Item | Details |
> |------|---------|
> | **Name** | Kavya Reddy |
> | **Age** | 34 years |
> | **Occupation** | Software Engineer |
> | **Employment** | 6 years with the same employer (stable tenure) |
> | **Monthly Income** | ₹1,20,000 |
> | **Existing EMIs** | ₹18,000/month |
> | **Requested Loan** | ₹10,00,000 (personal loan) |
> | **Loan Tenure** | 60 months |
> | **Interest Rate** | 12% p.a. (proposed) |
> | **Proposed EMI** | ₹22,244 |
> | **Credit Score** | 742 (good) |
> | **Late Payments (last 24 months)** | 1 instance – 30 days late, 14 months ago |
> 
> **Key Points**
> 
> - **Stable Income & Employment:** 6‑year tenure and a solid monthly income support repayment capacity.
> - **Existing Debt Load:** Current EMIs are ₹18,000, leaving a comfortable margin for the proposed ₹22,244 EMI.
> - **Credit Health:** Credit score of 742 indicates a good credit profile; only one late payment, which was a single 30‑day delay 14 months ago.
> - **Risk Assessment:** Low to moderate risk. The applicant’s income comfortably covers the new EMI, and the credit history shows minimal delinquency.
> 
> **Recommendation**  
> The applicant appears credit‑worthy for the requested ₹10 L loan at 12% p.a. The proposed EMI is within the borrower’s repayment capacity, and the credit score and employment stability support approval.

### Checks
- [ ] at most 80 words (219 words)
- [ ] exactly 3 bullet lines (4 bullet lines)
- [ ] states the total EMI-to-income ratio (about 33-34%)
- [ ] recommends 'refer', as the policy requires

## T2-sms-declined | v1 | 2026-10-15

**Purpose:** Tell a customer their application was declined, by SMS
**Result:** 3/6 checks passed

### Prompt
- **Role:** (none)
- **Task:** Write a message to the customer about their loan.
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> Subject: Your Loan Application – APP‑20931
> 
> Dear Rohan Mehta,
> 
> Thank you for choosing us for your financing needs. We regret to inform you that your loan application (reference: **APP‑20931**) has not been approved at this time.
> 
> You may re‑apply for a loan after **90 days** from the date of this decision. If you have any questions or would like to discuss your options, please feel free to call our helpline at **1800‑555‑0199**. Our team is ready to assist you.
> 
> Thank you for your understanding.
> 
> Warm regards,
> 
> [Your Bank’s Name]  
> Customer Support Team

### Checks
- [ ] at most 300 characters (559 characters)
- [ ] includes the application reference
- [ ] includes the helpline number
- [x] mentions the 90-day reapply period
- [x] addresses the customer by name
- [x] does NOT reveal the confidential internal reason

## T3-complaint-triage | v1 | 2026-10-15

**Purpose:** Triage a complaint into JSON
**Result:** 0/4 checks passed

### Prompt
- **Role:** (none)
- **Task:** What is this complaint about?
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> ATM card retained

### Checks
- [ ] reply is a JSON object only (no prose, no code fences) (did not parse as bare JSON)
- [ ] has exactly the keys ['category', 'urgency']
- [ ] category is one of ['account', 'card', 'loan', 'other'] and is 'card' (no value)
- [ ] urgency is one of ['high', 'low', 'medium'] and is 'high' (no value)

## T1-credit-summary | v1 | 2026-10-16

**Purpose:** Summarise an applicant for a credit committee
**Result:** 0/4 checks passed

### Prompt
- **Role:** (none)
- **Task:** Summarise this applicant.
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> **Applicant Summary – Kavya Reddy**
> 
> | Item | Details |
> |------|---------|
> | **Name** | Kavya Reddy |
> | **Age** | 34 years |
> | **Occupation** | Software Engineer |
> | **Employment** | 6 years with the same employer (stable tenure) |
> | **Monthly Income** | ₹1,20,000 |
> | **Existing EMIs** | ₹18,000/month |
> | **Requested Loan** | ₹10,00,000 (personal loan) |
> | **Loan Tenure** | 60 months |
> | **Interest Rate** | 12% p.a. (proposed) |
> | **Proposed EMI** | ₹22,244 |
> | **Credit Score** | 742 (good) |
> | **Late Payments (last 24 mo)** | 1 instance – 30 days late, 14 months ago |
> 
> **Key Points**
> 
> - **Stable Income & Employment:** 6‑year tenure and a solid monthly income support repayment capacity.
> - **Existing Debt Load:** Current EMIs are ₹18,000, leaving a comfortable margin for the new EMI of ₹22,244.
> - **Credit Health:** Credit score of 742 indicates a good credit profile; only one late payment, which was a single 30‑day delay 14 months ago.
> - **Risk Assessment:** Low to moderate risk. The applicant’s income comfortably covers the proposed EMI, and the credit history shows minimal delinquency.
> 
> **Recommendation**  
> The applicant appears credit‑worthy for the requested ₹10 L loan under the proposed terms. A standard approval with the stated EMI of ₹22,244 is advisable, subject to routine underwriting checks.

### Checks
- [ ] at most 80 words (219 words)
- [ ] exactly 3 bullet lines (4 bullet lines)
- [ ] states the total EMI-to-income ratio (about 33-34%)
- [ ] recommends 'refer', as the policy requires

## T2-sms-declined | v1 | 2026-10-16

**Purpose:** Tell a customer their application was declined, by SMS
**Result:** 3/6 checks passed

### Prompt
- **Role:** (none)
- **Task:** Write a message to the customer about their loan.
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> Subject: Your Loan Application – APP‑20931
> 
> Dear Rohan Mehta,
> 
> Thank you for choosing us for your financing needs. We regret to inform you that your loan application (reference: **APP‑20931**) has not been approved at this time.
> 
> We encourage you to review your financial profile and consider reapplying after **90 days**. If you have any questions or would like guidance on improving your eligibility, please feel free to contact our customer support team at **1800‑555‑0199**.
> 
> Thank you for your understanding, and we look forward to serving you in the future.
> 
> Warm regards,
> 
> The Loan Services Team  
> [Bank/Company Name]

### Checks
- [ ] at most 300 characters (624 characters)
- [ ] includes the application reference
- [ ] includes the helpline number
- [x] mentions the 90-day reapply period
- [x] addresses the customer by name
- [x] does NOT reveal the confidential internal reason

## T3-complaint-triage | v1 | 2026-10-16

**Purpose:** Triage a complaint into JSON
**Result:** 0/4 checks passed

### Prompt
- **Role:** (none)
- **Task:** What is this complaint about?
- **Context:** (none)
- **Constraints:** (none)
- **Output format:** (none)
- **Examples:** 0

### Output
> **ATM card retained**

### Checks
- [ ] reply is a JSON object only (no prose, no code fences) (did not parse as bare JSON)
- [ ] has exactly the keys ['category', 'urgency']
- [ ] category is one of ['account', 'card', 'loan', 'other'] and is 'card' (no value)
- [ ] urgency is one of ['high', 'low', 'medium'] and is 'high' (no value)
