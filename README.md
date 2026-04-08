MAP Compliance Monitoring System

Overview

This project implements a rule-based analytics system to monitor and enforce Minimum Advertised Price (MAP) compliance across multiple marketplaces and product categories.

The system detects pricing violations in near real-time using predefined business rules and generates actionable insights to support pricing governance and brand protection.

⸻

Business Problem

Brands enforce MAP policies to maintain pricing integrity across marketplaces. However, sellers often violate these rules during promotions or discount periods.

Key Challenges
	•	Detecting violations across large-scale product listings
	•	Handling dynamic pricing and promotional campaigns
	•	Ensuring consistent enforcement across marketplaces

Risks of Non-Compliance
	•	Brand value erosion
	•	Price wars across sellers
	•	Revenue and margin loss

⸻

Dataset Description

Overview

This project uses a structured, multi-table dataset to simulate MAP compliance monitoring across products, sellers, and marketplaces.

The dataset reflects real-world pricing scenarios, including MAP pricing, promotions, and seller mappings.

⸻

Data Privacy & Anonymization

To ensure confidentiality and align with data governance best practices, sensitive fields have been anonymized:
	•	SKU values → replaced with product_id
	•	Seller names → replaced with seller_id
	•	Homologated seller names → replaced with homologated_seller_id

These transformations preserve relational integrity while protecting sensitive business information.

⸻

Dataset Structure

1. Product Mapping
	•	Maps internal product numbers to standardized product_id
	•	Ensures consistent product reference across all tables

2. Product & Category Data
	•	Product Line (PL)
	•	Category
	•	Subcategory

3. Pricing Data
	•	MAP Price (map_price)
	•	Purchase Price
	•	Used for identifying pricing violations

4. Promotion Data
	•	Seasonal promotions (Q1–Q4)
	•	Includes:
	•	Percentage discounts
	•	Fixed discounts
	•	Bundle offers

5. Seller Mapping
	•	Maps sellers to homologated identifiers
	•	Enables seller-level compliance tracking

⸻

Notes
	•	Dataset is a sample subset of a larger dataset
	•	Includes both compliant and violation scenarios
	•	Covers edge cases (missing values, boundary conditions)
	•	Data is anonymized due to confidentiality

⸻

Violation Rules

Rule 1: Promotion Violation

Condition:
	•	Season = Q2
	•	Promotion is active

Violation:
	•	Advertised Price < Promotion Price

⸻

Rule 2: MAP Violation

Condition:
	•	Advertised Price < MAP Price

⸻

Approach
	1.	Data ingestion and cleaning
	2.	Rule-based validation engine
	3.	Violation tagging and classification
	4.	Aggregation across category and marketplace
	5.	Reporting and insights generation

⸻

Tech Stack
	•	Python, Pandas, NumPy
	•	SQL

⸻

Key Features
	•	Automated detection of MAP violations
	•	Scalable rule-based engine
	•	Marketplace and category-level monitoring
	•	Structured outputs for compliance tracking
	•	Supports auditing and reporting workflows

⸻

Output & Insights
	•	Violation counts by marketplace
	•	Category-level compliance trends
	•	Seller-level violation tracking
	•	Time-based violation patterns

⸻

Enforcement Actions

Based on detected violations, the system supports:
	•	Violation notices for first-time offenders
	•	Warning letters for repeated violations
	•	Suspension actions for critical non-compliance

These templates simulate real-world compliance workflows used in e-commerce platforms.

⸻

Business Impact
	•	Improved pricing compliance monitoring
	•	Faster identification of violating sellers
	•	Supports enforcement actions (e.g., category suspension)
	•	Protects brand pricing strategy and margins

⸻

Future Work
	•	Real-time pipeline using streaming data
	•	ML-based anomaly detection
	•	Automated alert system
	•	Integration with compliance tools

⸻

Deployment (Optional)
	•	Streamlit (interactive app)
	•	Dashboard tools (if extended)

⸻

Why This Project Matters

MAP compliance is a critical function in e-commerce and retail analytics.

This project demonstrates:
	•	Strong understanding of business rules → data translation
	•	Ability to build scalable analytics systems
	•	Practical experience in real-world pricing governance