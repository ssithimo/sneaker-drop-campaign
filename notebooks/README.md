# Foot Locker Sneaker Drop 📬 A/B Subject Line Test

## 🧠 Project Overview
This project tests the effectiveness of two subject lines for a Foot Locker 
sneaker drop email campaign. The goal is to identify which subject line drives 
stronger customer engagement and downstream revenue by analyzing the full 
conversion funnel from inbox open to purchase.

## 📧 Test Variants
- **Email A (Control):** "Hurry! Limited pairs remaining."
- **Email B (Variant):** "Drop alert 🔥 Your exclusive access inside."

The **email content is identical** across both groups, isolating the effect of 
the subject line on open behavior and downstream funnel performance.

## 📊 Methodology
- Simulated dataset of 20,000 users (10,000 per group)
- Full funnel simulation: opens → clicks → purchases → revenue
- Fixed average order value of $180, consistent with mid-tier limited-edition sneaker retail pricing
- Conducted **two-proportion z-tests** on both open rates and purchase conversion rates to assess statistical significance
- Revenue bridge constructed to quantify incremental business impact at scale

## ✅ Key Findings

### Open Rate
- Email B produced a statistically significant higher open rate (27.58% vs. 
  24.13%, p < 0.001), confirming the hype-driven subject line more effectively 
  captures inbox attention

### Funnel Decomposition
- Despite losing on open rate, Email A's openers converted to clicks at a 
  higher rate (11.19% vs. 9.39% CTOR), suggesting the urgency framing 
  self-selected for higher-intent readers already predisposed to engage
- Overall CTR slightly favored Email A (2.70% vs. 2.59%), illustrating that 
  open rate alone does not determine downstream click volume — audience 
  composition matters
- This highlights a key limitation of overall CTR as a standalone metric: it 
  conflates subject line and content effectiveness into a single number, masking 
  where each variant won and lost

### Purchase Conversion
- Email B produced more purchases (56 vs. 46) and higher revenue 
  ($10,080 vs. $8,280) in this simulation run
- However, a two-proportion z-test on purchase conversion rates failed to reach 
  statistical significance (z = -1.34, p = 0.1815)
- We fail to reject H₀ that purchase conversion rates are equal between groups — 
  the observed difference is within expected random variation given the smaller 
  sample of ~260 clickers per group

### Revenue Bridge
- Incremental revenue from Email B assumes the observed purchase advantage holds:

| Subscriber List Size | Incremental Revenue |
|----------------------|-------------------|
| 50,000               | $9,000            |
| 100,000              | $18,000           |
| 500,000              | $90,000           |

- These projections represent potential upside if B's revenue advantage proves 
  consistent across future campaigns, which is not a guaranteed outcome from this 
  single test

## 📝 Conclusion
Email B is the recommended subject line for future sneaker drop campaigns based 
on its statistically significant open rate advantage (p < 0.001). A higher open 
rate means more recipients entering the funnel on every send, which is a compounding 
benefit across a full campaign calendar.

However, three important caveats apply:

1. **Revenue conclusions are premature.** The purchase conversion difference 
   between groups was not statistically significant (p = 0.1815). B's revenue 
   advantage in this run is attributable to random variation, not a confirmed 
   systematic effect. Live campaign data with larger click volumes is needed 
   before making revenue-based subject line decisions.

2. **Audience quality tradeoff exists.** Email A's higher CTOR suggests its 
   urgency framing attracts higher-intent openers. Future tests should explore 
   whether combining urgency and hype elements could capture both effects 
   simultaneously.

3. **Downstream metrics require ongoing monitoring.** CTOR, conversion given 
   click, and overall CVR should be tracked on every future send to detect 
   whether B's opener quality holds steady over time.

## 📁 Files
- `sneaker_drop_email_ab_data.csv`: Simulated dataset
- `sneaker_drop_email_campaign.ipynb`: Full analysis including simulation, 
  EDA, funnel decomposition, hypothesis testing, and revenue bridge
