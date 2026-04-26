# Will the Customer Accept the Coupon?

## Overview

This project explores a dataset collected via an Amazon Mechanical Turk survey that describes different driving scenarios and asks whether the driver would accept a coupon delivered to their phone. The goal is to use data analysis and visualizations to understand what distinguishes drivers who accept coupons from those who do not.

**Dataset source:** UCI Machine Learning Repository
**Notebook:** [cust_coupn_acceptance.ipynb](cust_coupn_acceptance.ipynb)

---

## Key Findings

### Overall Coupon Acceptance
Approximately **57% of all coupons** in the dataset were accepted. Coupon type, weather, time of day, and who is in the car all play meaningful roles in whether a driver accepts.

- **Carry Out & Take Away** and **cheap restaurant** coupons had the highest acceptance rates.
- **Bar** coupons had the lowest overall acceptance rate (~41%).
- Drivers heading to "no urgent place" and those accompanied by friends or a partner were most receptive to any coupon.
- Sunny weather and warmer temperatures (80°F) correlated with higher acceptance.

---

### Bar Coupons
The single strongest predictor of bar coupon acceptance is **how often someone already visits bars**.

- Drivers who visit bars **more than 3 times a month** accept bar coupons at a rate of ~77%, compared to ~37% for infrequent bar-goers.
- Younger drivers (under 30) who frequently visit bars are especially likely to accept.
- Having kids in the car significantly reduces acceptance — drivers in family contexts are far less likely to detour to a bar.
- Widowed individuals showed notably lower acceptance than other marital status groups.

**Recommendation:** Target bar coupons at frequent bar-goers aged 21–30 who are traveling without children.

---

### Coffee House Coupons
Coffee House is the most common coupon type. Key predictors of acceptance:

- **Visit frequency** is again the top factor — drivers who already visit coffee houses at least once a month accept coupons at much higher rates.
- **Time of day matters:** Coupons sent at 10AM or 2PM see higher acceptance than evening offers, which aligns with typical coffee drinking habits.
- **Social context:** Drivers with friends or a partner in the car are more likely to stop for coffee than those driving alone or with kids.
- **Coupon expiration:** 1-day expiration coupons outperform 2-hour coupons — drivers prefer flexibility.

**Recommendation:** Send coffee house coupons to habitual coffee drinkers in the morning or early afternoon, especially when they are with friends or a partner.

---

## Actionable Recommendations

| Coupon Type | Best Target Profile | Avoid |
|-------------|--------------------|----|
| Bar | Frequent bar-goers, age 21–30, no kids in car | Drivers with kids, widowed individuals |
| Coffee House | Habitual coffee drinkers, 10AM–2PM, social passengers | Evening, solo drivers who never visit coffee houses |
| All coupons | No-urgent-destination trips, sunny weather | Drivers on urgent trips to work/home |

---

## Project Structure

```
uc-da-cust-coupon/
├── cust_coupn_acceptance.ipynb         # Main analysis notebook
├── README.md            
└── data/
    └── coupons.csv      # Raw dataset
```

---

## Tools & Libraries

- **Python 3**
- **pandas** — data loading, cleaning, and grouping
- **matplotlib** — custom plots and subplots
- **seaborn** — statistical visualizations and heatmaps
- **numpy** — numerical operations
