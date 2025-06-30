

## 🚌 Hackathon Challenge Summary

The objective of this hackathon is to **forecast seat demand for bus journeys** at the route level, exactly **15 days before the actual date of journey (DOJ)**.

### 🔍 Problem Overview

Demand for bus journeys is affected by a wide range of factors such as:

* National and regional holidays
* Long weekends
* Wedding seasons
* School vacations and exam schedules
* Day-of-week effects

However, not all holidays significantly impact demand, making this a **non-trivial time series forecasting problem**.

### 🎯 Your Task

Using the historical data provided, you need to develop a predictive model that estimates the **total number of seats that will be booked** for a given route on a specific DOJ, based on data available **15 days prior**.

For example, for a route from City A to City B with a DOJ on *30-Jan-2025*, your prediction should be made on *15-Jan-2025*, using only data available up to that point.

---

## 📁 Dataset Description

### 1. `train.csv`

| Variable          | Description                                                                    |
| ----------------- | ------------------------------------------------------------------------------ |
| `doj`             | The date on which the bus journey is scheduled to take place.                  |
| `srcid`           | Unique identifier for the source city of the journey.                          |
| `destid`          | Unique identifier for the destination city of the journey.                     |
| `final_seatcount` | Total number of seats booked at the end of the journey date (Target Variable). |

---

### 2. `test.csv`

| Variable    | Description                                                   |
| ----------- | ------------------------------------------------------------- |
| `route_key` | Unique identifier for each row in the test set.               |
| `doj`       | The date on which the bus journey is scheduled to take place. |
| `srcid`     | Unique identifier for the source city of the journey.         |
| `destid`    | Unique identifier for the destination city of the journey.    |

---

### 3. `transactions.csv`

| Variable             | Description                                                         |
| -------------------- | ------------------------------------------------------------------- |
| `doj`                | The date on which the bus journey is scheduled to take place.       |
| `doi`                | The date when the ticket was booked.                                |
| `dbd`                | Days before departure (i.e., DOJ - DOI).                            |
| `srcid`              | Unique identifier for the source city.                              |
| `destid`             | Unique identifier for the destination city.                         |
| `srcid_region`       | Region (state) where the source city is located.                    |
| `destid_region`      | Region (state) where the destination city is located.               |
| `srcid_tier`         | Tier classification of the source city (e.g., Tier 1, Tier 2).      |
| `destid_tier`        | Tier classification of the destination city.                        |
| `cumsum_seatcount`   | Cumulative number of seats sold till the date of issue.             |
| `cumsum_searchcount` | Cumulative number of searches for the route till the date of issue. |

---

