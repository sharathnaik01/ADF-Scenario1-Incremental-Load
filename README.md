# ADF-Scenario1-Incremental-Load🚀 📌

🚀 **Incremental Loading Pipeline using Azure Data Factory & Azure Data Lake Storage**

This repository contains the implementation of **Scenario-1: Incremental Loading** in **Azure Data Factory (ADF)** using **Azure Data Lake Storage Gen2** as the source.

---

## 📌 Overview

In modern data engineering, incremental loading helps improve performance by transferring **only new or updated records** instead of full dataset reloads.  
This pipeline uses ADF activities such as:
- **Get Metadata**
- **If Condition**
- **Copy Data**
- **Variables and Parameters**

---

## 🔧 Features

- ✅ Ingests only new/modified files from ADLS
- ✅ Uses file `lastModified` timestamp for comparison
- ✅ Reduces data load time and cost
- ✅ Ideal for large-scale batch processing scenarios

---

## 🗂 Folder Structure
ADF-Scenario1-Incremental-Load/
│
├── datasets/
│   └── your-dataset-name.json

├── linkedServices/
│   └── your-linkedservice-name.json

├── pipelines/
│   └── ADF-Scenario1-Incremental-Load.json

├── output.png
└── README.md


---

## 🛠 Tech Stack

| Component           | Description                           |
|--------------------|---------------------------------------|
| Azure Data Factory | Orchestration and pipeline logic      |
| Azure Data Lake Gen2 | Source storage system               |
| GitHub             | Version control                       |

---

## ⚙️ How It Works

1. **Get Metadata Activity**: Checks the latest file's `lastModified` timestamp from ADLS.
2. **Compare Timestamps**: Compares current file's timestamp with stored value.
3. **Condition Activity**: If a newer file exists, triggers the Copy Data activity.
4. **Copy Data**: Moves only the incremental data to destination.
5. **Set Variable Activity**: Updates max timestamp for next run.

---

## 📸 Output Snapshot

Below is the execution output of the **Incremental Load pipeline** in Azure Data Factory:

### 📸 Output Snapshot

Below is the execution output of the **Incremental Load pipeline** in Azure Data Factory:
![Output](https://github.com/user-attachments/assets/126cc01a-e940-4d39-ac5a-9bce2bf11506)
Pipeline  of ADF-Scenario1-Incremental-Load🚀 📌
![pieline image](https://github.com/user-attachments/assets/a77d5b3d-0096-4a3f-927d-b1b9d8d26084)


## 📈 Use Case

This pipeline is especially useful for:
- Daily ingestion of log files
- Delta loads from cloud-based sources
- Scheduled batch ETL workflows

---

## ✍ Author

**Sharath Naik**  
Data Engineer | Cloud & Big Data Enthusiast  | cloud Support Engineer
📫 [LinkedIn](https://www.linkedin.com/in/sharath-naik)

---

## 📝 License

This project is open source and free to use under the MIT License.

---
