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

### 🥉 Bronze Layer
- Raw JSON files from the web
- Unzipped and stored in Lakehouse

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

---

## 📁 Project Structure

![image](https://github.com/user-attachments/assets/f688fd4b-3941-4adb-a876-8484d7b9d523)

---

## ▶️ How to Run

> Ensure you have access to **Microsoft Fabric** and a configured Lakehouse.

1. Run the Get Files and Process Pipeline

---

## 🔮 Future Improvements

- 

---

## ✨ Acknowledgements

- - IPL data by [CricSheet.org](https://cricsheet.org/)

