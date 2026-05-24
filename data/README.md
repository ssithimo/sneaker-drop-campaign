# 📊 Dataset Description

This dataset simulates an email marketing A/B test for Foot Locker’s limited-edition sneaker drop campaign. It includes data for 20,000 recipients split evenly into two groups, each receiving a different email subject line variant.

---

📌 NOTE 


The data is synthetically generated with realistic open and click-through probabilities to mimic typical email campaign engagement.

🤔 Assumptions:
  - Subject‑line variants A is baseline version (control), B is variant
  - 25 % open rate – Urgency line
  - 27 % open rate – Hype/emoji line
  - 12 % click‑through given open (Group A)
  - 10 % click‑through given open (Group B)
  - 20 % purchase given click
  - $180 average order value (midpoint limited edition sneaker price ranges from 150 - 220)

The code can be found here [Sneaker Drop Email Campaign Data Code](https://github.com/ssithimo/sneaker-drop-campaign/edit/main/data/sneaker_drop_email_campaign_data)

The csv file can be found here [Sneaker Drop Email Campaign Data](https://github.com/ssithimo/sneaker-drop-campaign/blob/main/data/sneaker_drop_email_ab_data.csv)

---

🗄 Data:


user_id 🆔 : Unique ID for each email recipient

group 👫 : Experimental group assignment (A = urgency-based subject line, B = hype-based subject line)

opened 📬 : Whether the email was opened (1 = yes, 0 = no)

clicked 🖱️ : Whether a link inside the email was clicked (1 = yes, 0 = no; click can only happen if opened)

purchased 💵 : Whether a purchase was made (1 = yes, 0 = no; purchase can only happen if clicked)

