# ✈️ Flight Status Dashboard (Power BI)

> An end-to-end Power BI Business Intelligence project analyzing **1.9 million US domestic flight records** to uncover trends in airline performance, delays, cancellations, and airport traffic through an interactive dashboard.

---

# 📖 Project Overview

This project demonstrates the complete Power BI development lifecycle—from importing raw datasets to building a fully interactive dashboard.

The project showcases:

- Data Import & Cleaning using Power Query
- Data Transformation
- Relational Data Modeling
- DAX Measure Creation
- Dashboard Design
- Business Intelligence & Data Visualization
- Version Control using Git & GitHub

The dashboard enables users to analyze:

- Total flights
- Delayed flights
- Cancelled flights
- Airport traffic
- Airline delay percentages
- Flight status distribution
- Cancellation reasons

---

# 📊 Dashboard Preview

> Replace the image below with a screenshot of your dashboard after uploading it to the repository.

```md
![Dashboard](dashboard.png)
```

---

# 🎯 Project Objectives

The objective of this project was to:

- Analyze airline operational performance
- Compare airline delay percentages
- Identify the busiest airports
- Understand cancellation trends
- Practice dimensional modeling in Power BI
- Build an executive-style dashboard
- Demonstrate an end-to-end Business Intelligence workflow

---

# 📂 Repository Structure

```text
US-Flight-Performance-Dashboard/
│
├── 📁 data/
│   ├── airlines.csv
│   ├── airports.csv
│   ├── cancellation_codes.csv
│   └── flights.csv
│
├── 📄 flight-status-dashboard.pbix
│
├── 📄 README.md
│
└── 📄 .gitignore
```

### Repository Contents

| Item | Description |
|------|-------------|
| **data/** | Contains all raw datasets used in the project. |
| **flight-status-dashboard.pbix** | Main Power BI file containing Power Query transformations, data model, DAX measures, and dashboard. |
| **README.md** | Project documentation. |
| **.gitignore** | Git ignore configuration. |

---

# 🌿 Git Branch Workflow

The project was developed incrementally using feature branches.

| Branch | Purpose |
|----------|----------|
| `01-blank-project` | Created the initial Power BI project |
| `02-importing-dataset_transforming_it` | Imported datasets and performed data cleaning & transformation |
| `03-building-relational-model` | Built the relational data model |
| `04-add-dax-measures` | Created DAX calculations and KPIs |
| `05-designing-a-dynamic-dashboard` | Designed the final interactive dashboard |
| `main` | Final completed project |

Using separate branches demonstrates a structured development workflow and version control practices.

---

# 📚 Dataset

The project uses four datasets.

## 1. Flights (Fact Table)

Contains the complete flight records.

### Key Columns

- Flight ID
- Year
- Month
- Day
- Day of Week
- Airline
- Flight Number
- Origin Airport
- Destination Airport
- Scheduled Departure
- Departure Time
- Departure Delay
- Scheduled Time
- Elapsed Time
- Distance
- Scheduled Arrival
- Arrival Time
- Arrival Delay
- Diverted
- Cancelled
- Cancellation Reason
- Air System Delay
- Security Delay
- Airline Delay
- Late Aircraft Delay

---

## 2. Airlines (Dimension Table)

Maps airline codes to airline names.

| Column |
|---------|
| IATA Code |
| Airline |

Example:

| Code | Airline |
|------|------------------------------|
| DL | Delta Air Lines |
| UA | United Air Lines |
| WN | Southwest Airlines |
| AA | American Airlines |

---

## 3. Airports (Dimension Table)

Contains airport metadata.

Columns include:

- Airport
- City
- State
- Country
- Latitude
- Longitude
- IATA Code

---

## 4. Cancellation Codes (Dimension Table)

Maps cancellation reason codes to readable descriptions.

| Code | Description |
|------|-------------|
| A | Airline / Carrier |
| B | Weather |
| C | National Air System |
| D | Security |

---

# 🧹 Data Preparation

Before creating the dashboard, the datasets were prepared using Power Query.

Typical transformations included:

- Importing CSV datasets
- Verifying data types
- Cleaning inconsistent values
- Renaming columns where required
- Building relationships
- Preparing data for DAX calculations

---

# 🗂 Data Model

The project follows a **Star Schema**.

```text
                  Airlines
                      │
                      │
Airports ─────── Flights ─────── Cancellation Codes
```

The **Flights** table acts as the Fact Table while the remaining tables serve as Dimension Tables.

---

# 🔗 Relationships

| From | To | Relationship |
|------|----|--------------|
| Airlines[IATA_CODE] | Flights[AIRLINE] | One-to-Many |
| Airports[IATA_CODE] | Flights[ORIGIN_AIRPORT] | One-to-Many |
| Cancellation Codes[CANCELLATION_REASON] | Flights[CANCELLATION_REASON] | One-to-Many |

---

# 📐 DAX Measures

Several DAX measures were created to calculate KPIs dynamically.

Examples include:

- Total Flights
- Delayed Flights
- Cancelled Flights
- On-Time Flights
- Delay Percentage
- Cancellation Percentage
- On-Time Percentage
- Airline Delay Percentage

These measures automatically update based on report filters and slicers.

---

# 📈 Dashboard Components

## ✈️ KPI Cards

Displays:

- Total Flights
- Delayed Flights
- Cancelled Flights

---

## 🛫 Airport Traffic

Ranks airports based on total flight volume.

Highlights the busiest airports such as:

- Atlanta
- Chicago
- Dallas/Fort Worth
- Denver
- Los Angeles

---

## ⏱ Airline Delay Performance

Ranks airlines according to delay percentage, making it easy to compare operational performance.

---

## ❌ Cancellation Analysis

Displays cancellation reasons using a donut chart.

Reasons include:

- Airline / Carrier
- Weather
- National Air System
- Security

---

## 📊 Flight Status Summary

Shows the percentage of flights that were:

- On-Time
- Delayed
- Cancelled

---

## 📉 Dynamic Status Bar

Provides a visual comparison of:

- On-Time Flights
- Delayed Flights
- Cancelled Flights

---

# 📊 Key Insights

Some notable insights from the dashboard include:

- Approximately **1.9 million** flights were analyzed.
- Around **791 thousand** flights experienced delays.
- Approximately **28 thousand** flights were cancelled.
- Atlanta handled the highest number of flights.
- Weather accounted for a significant proportion of cancellations.
- Airline delay percentages varied considerably across carriers.

---

# 🛠 Technologies Used

- Microsoft Power BI
- Power Query
- DAX (Data Analysis Expressions)
- Data Modeling
- Star Schema
- Git
- GitHub

---

# 💡 Skills Demonstrated

- Data Cleaning
- Data Transformation
- Data Modeling
- Relational Database Design
- Star Schema Implementation
- DAX
- KPI Development
- Interactive Dashboard Design
- Business Intelligence
- Data Visualization
- Data Storytelling
- Git Version Control

---

# 🚀 Learning Outcomes

This project strengthened my understanding of:

- Importing and transforming datasets
- Building relational data models
- Creating reusable DAX measures
- Designing interactive dashboards
- Applying Business Intelligence best practices
- Using Git branches to manage project development

---

# 🔮 Future Improvements

Potential enhancements include:

- Interactive drill-through pages
- Time-series trend analysis
- Airport location map visualizations
- Flight route analysis
- Delay prediction using Machine Learning
- Additional report pages for airline-specific insights

---

# 📸 Project Screenshots

## Dashboard

```md
![Dashboard](dashboard.png)
```

## Data Model

```md
![Data Model](data_model.png)
```

## Flights Table

```md
![Flights Table](flights_table.png)
```

## Airlines Table

```md
![Airlines Table](airlines_table.png)
```

## Airports Table

```md
![Airports Table](airports_table.png)
```

## Cancellation Codes Table

```md
![Cancellation Codes](cancellation_codes_table.png)
```

---

# 📬 Contact

If you have any questions, suggestions, or feedback regarding this project, feel free to open an issue or connect with me on GitHub.

---

# ⭐ Support

If you found this project helpful or interesting, consider giving the repository a **⭐ Star**. It helps others discover the project and supports my portfolio.
