# 📊 Meta Ad Performance Analysis | Power BI

## 📌 Project Overview

This project presents an interactive **Meta Ad Performance Dashboard developed in Power BI** to analyze paid advertising campaigns running across **Facebook and Instagram**.

The dashboard provides an end-to-end view of advertising performance, from **impressions and clicks to engagement and purchases**, while also allowing users to analyze campaign performance across audience demographics, geographic locations, ad formats, campaigns, interests, and time periods.

The primary objective of the project is to transform raw advertising interaction data into meaningful business insights that can help marketing teams evaluate campaign effectiveness, understand audience behavior, identify high-performing ad formats, and make better budget allocation decisions.

---

## 🎯 Business Objective

The dashboard was developed to help answer key marketing questions such as:

- How effectively are advertisements generating impressions, clicks, and engagement?
- How efficiently are clicks converting into purchases?
- Which audience segments generate the highest engagement?
- Which countries contribute the most advertising activity?
- Which ad formats perform best?
- At what times of the day is engagement highest?
- How does campaign performance change over time?
- Where can advertising strategy and budget allocation be improved?

The analysis focuses specifically on **paid Facebook and Instagram advertising campaigns**.

---

## 🛠️ Tools & Technologies

- **Power BI**
- **Power Query**
- **DAX**
- **Data Modeling**
- **Data Visualization**
- **Interactive Slicers & Filters**
- **Dynamic Measure Selection**
- **Calendar / Date Analysis**
- **Geospatial Analysis**

---

## 🗂️ Dataset Overview

The data model contains four primary tables:

### 1. `ad_events`
The main fact table containing individual user interactions with advertisements.

Important fields include:

- `event_id`
- `ad_id`
- `user_id`
- `timestamp`
- `day_of_week`
- `time_of_day`
- `event_type`

The event data captures activities such as:

- Impression
- Click
- Share
- Comment
- Purchase

---

### 2. `ads`
Contains advertisement-level information including:

- `ad_id`
- `campaign_id`
- `ad_platform`
- `ad_type`
- `target_gender`
- `target_age_group`
- `target_interests`

This table enables analysis by advertising platform, creative format, and target audience.

---

### 3. `campaigns`
Contains campaign-level information such as:

- `campaign_id`
- `name`
- `start_date`
- `end_date`
- `duration_days`
- `total_budget`

This table supports campaign-level filtering and budget analysis.

---

### 4. `users`
Contains demographic and geographic information about users interacting with advertisements.

Important fields include:

- `user_id`
- `user_gender`
- `user_age`
- `age_group`
- `country`
- `location`
- `interests`

This enables demographic, geographic, and audience segmentation analysis.

---

## 🔗 Data Model

The dashboard uses a fact-and-dimension style data model.

```text
                    campaigns
                        │
                        │ campaign_id
                        ▼
ads ◄──────────── campaign relationship
 │
 │ ad_id
 ▼
ad_events
 │
 │ user_id
 ▼
users
