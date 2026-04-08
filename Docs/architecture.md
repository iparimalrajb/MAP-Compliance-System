# System Architecture – MAP Compliance Monitoring

This document describes the overall workflow and structure of the MAP Compliance Monitoring System.

---

## Overview

The system processes pricing data, applies business rules, and generates violation outputs along with enforcement actions.

---

## Workflow

1. Data Ingestion  
   - Load processed datasets (price list, promotions, seller mapping)

2. Data Preprocessing  
   - Clean missing values  
   - Standardize column formats  

3. Data Integration  
   - Merge multiple datasets into a unified pricing table  

4. Rule Engine  
   - Apply MAP and Promotion violation logic  
   - Tag violations with type and severity  

5. Output Generation  
   - Generate violation tables  
   - Store results for reporting and action  

6. Action Layer  
   - Generate violation, warning, or suspension letters  

---

## Components

### 1. Data Layer
- Processed CSV files  
- Structured pricing and promotion data  

### 2. Processing Layer
- Pandas-based transformations  
- Data merging and filtering  

### 3. Rule Engine
- Encapsulated logic for violation detection  
- Modular and scalable design  

### 4. Output Layer
- Violation tables  
- Price monitoring tables  

### 5. Action Layer
- Automated letter templates  
- Supports compliance enforcement  

---

## Folder Mapping

- `data/processed/` → Input data  
- `notebooks/` → Analysis and workflow  
- `src/` → Core logic (rule engine)  
- `outputs/` → Final results  
- `actions/` → Enforcement templates  
- `docs/` → System documentation  

---

## Scalability Considerations

- Easily extendable for new rules  
- Can integrate with real-time data pipelines  
- Can be connected to dashboards or alert systems  

---

## Future Enhancements

- Real-time monitoring using streaming data  
- ML-based anomaly detection  
- Automated alert notifications  
- Integration with compliance dashboards  

---