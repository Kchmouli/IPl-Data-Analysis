# 🏏 IPL Data Engineering Project

This project performs end-to-end data engineering and analytics on Indian Premier League (IPL) matches using **PySpark** on **Microsoft Fabric**. It implements the **Medallion Architecture** to transform raw web data into a clean star schema ready for analysis.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [Data Pipeline](#data-pipeline)
- [Project Structure](#project-structure)
- [How to Run](#how-to-run)
- [Future Improvements](#future-improvements)
- [License](#license)

---

## 📖 Overview

- **Goal**: Enable rich data analysis of IPL matches, players, and teams using a structured pipeline.
- **Source Data**: JSON files scraped from the web (match data, player stats, etc.)
- **Final Output**: Star schema with fact and dimension tables for analytics (Gold Layer)

---

## 🏗 Architecture

Web (JSON) --> Bronze: Raw JSON ingestion --> Silver: Cleaned & structured tables --> Gold: Star schema (Fact + Dimensions)

> Built on the **Medallion Architecture** (Bronze → Silver → Gold)

---

## 🧰 Tech Stack

| Layer            | Technology                      |
|------------------|---------------------------------|
| Platform         | Microsoft Fabric                |
| Language         | PySpark (Spark Notebooks)       |
| Storage          | Delta Lake (Lakehouse)          |
| Architecture     | Medallion (Bronze/Silver/Gold)  |
| Data Modeling    | Star Schema                     |

---

## 🔄 Data Pipeline
- Get Files and Process Pipeline
- Pipeline executes the three notebooks

![image](https://github.com/user-attachments/assets/c9e98bf8-0147-4eef-b233-abf88aaf105d)


### 🥉 Bronze Layer
- Raw JSON files from the web
- Unzipped and stored in Lakehouse
![image](https://github.com/user-attachments/assets/e80a6533-531d-4610-899b-c1693c274bed)


### 🥈 Silver Layer
- Cleaned and transformed data
- Flattened the nested JSON
- Table:
  - `innings_silver`

### 🥇 Gold Layer
- Star schema for analytics
- Tables:
  - `factInnings`
  - `dimPlayers`
  - `dimTeams`
  - `dimMatch`
  - `dimDismissal`

![image](https://github.com/user-attachments/assets/7334fa4a-20ec-45d9-a602-c999e66d8a34)


---

## 📁 Project Structure

![image](https://github.com/user-attachments/assets/f688fd4b-3941-4adb-a876-8484d7b9d523)
![image](https://github.com/user-attachments/assets/52ba4f30-f719-4ff2-b95e-5c127b1e3f4e)

---

## ▶️ How to Run

> Ensure you have access to **Microsoft Fabric** and a configured Lakehouse.

1. Run the Get Files and Process Pipeline

---

## 📊 Power BI Report

You can view the interactive IPL analytics report here:

[View IPL Analytics Power BI Report](https://app.powerbi.com/view?r=eyJrIjoiNTU0OTRlNjgtZGY4Ni00YWRhLTk1Y2ItYjhkYmMwZGU0YTViIiwidCI6IjIxNjJiMzEyLThkY2QtNDYyMC1iMGNlLTA1MzU1MmFlMzI5NCIsImMiOjF9&pageName=afb00c568cf044e3ebcd)

## 🔮 Future Improvements

- Need to intergrate current dataset with the above report

---

## ✨ Acknowledgements

- - IPL data by [CricSheet.org](https://cricsheet.org/)

