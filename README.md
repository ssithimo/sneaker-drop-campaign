# 👟 Foot Locker Sneaker Drop — A/B Subject Line Test

> *The variant with the higher open rate lost on clicks and why that 
> changes the recommendation 👀 *

---

## 🎯 Project Objective
Test two email subject lines for a Foot Locker limited-edition sneaker drop 
to identify which drives stronger engagement and downstream revenue across 
the full conversion funnel.

- **Email A (Control):** "Hurry! Limited pairs remaining."
- **Email B (Variant):** "Drop alert 🔥 Your exclusive access inside."

Email content was **identical** across both groups, isolating the subject 
line's effect on open behavior and downstream funnel performance.

---

## 📊 Methodology
- Simulated 20,000 users (10,000 per group) with full funnel tracking
- Metrics tracked: open rate, CTOR, overall CTR, purchase conversion, revenue
- Two-proportion z-tests on both open rates and purchase conversion rates
- Revenue bridge at $180 average order value to quantify incremental business impact at scale

---

## ✅ Key Findings

| Metric | Email A | Email B | Winner |
|--------|---------|---------|--------|
| Open Rate | 24.13% | 27.58% | B ✅ |
| CTOR | 11.19% | 9.39% | A ✅ |
| Overall CTR | 2.70% | 2.59% | A ✅ |
| Purchases | 46 | 56 | B ✅ |
| Revenue | $8,280 | $10,080 | B ✅ |

**Open rate (p < 0.001):** Email B's advantage is statistically significant — 
the hype-driven subject line demonstrably captures more inbox attention.

**CTOR:** Despite losing on opens, Email A's openers clicked at a higher rate 
(11.19% vs. 9.39%), suggesting urgency language self-selects for higher-intent 
readers. This is why Email B won on opens but lost on total clicks (259 vs. 270).

**Purchase conversion (p = 0.1815):** The difference in purchases is not 
statistically significant. B's revenue advantage reflects randomness in this simulation.

---

## 💰 Revenue Bridge
Assuming B's observed purchase advantage holds across future campaigns:

| Subscriber List Size | Incremental Revenue vs. Email A |
|----------------------|---------------------------------|
| 50,000 | $9,000 |
| 100,000 | $18,000 |
| 500,000 | $90,000 |

---

## 📝 Recommendation
**Roll out Email B** based on its statistically confirmed open rate advantage. 
More openers means more funnel entries on every send!

However:
- Revenue conclusions require live campaign validation
- Email A's higher CTOR suggests a hybrid subject line combining urgency and 
  hype could outperform both variants
- Downstream metrics (CTOR, conversion given click, CVR) should be monitored 
  on every future send

---

## 📁 Files
- `sneaker_drop_email_ab_data.csv` — Simulated dataset
- `sneaker_drop_email_campaign.ipynb` — Full analysis: simulation, EDA, 
  funnel decomposition, hypothesis testing, and revenue bridge
