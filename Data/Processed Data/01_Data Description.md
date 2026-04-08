Dataset Description

Overview

This project uses a structured, multi-table dataset to simulate MAP (Minimum Advertised Price) compliance monitoring across products, sellers, and marketplaces.

The dataset is designed to reflect real-world pricing scenarios, including MAP pricing, promotions, and seller mappings.

⸻

Data Privacy & Anonymization

To ensure confidentiality and align with data governance best practices, sensitive fields have been anonymized:
	•	SKU values have been replaced with synthetic product_id identifiers
	•	Seller names have been replaced with seller_id
	•	Homologated (partner) seller names have been replaced with homologated_seller_id

These transformations preserve relational integrity across datasets while protecting sensitive business information.

⸻

Dataset Structure

The dataset consists of the following components:

1. Product Mapping
	•	Maps internal product numbers to standardized product_id
	•	Ensures consistent product reference across all tables

⸻

2. Product & Category Data
	•	Contains product-level attributes such as:
	•	Product Line (PL)
	•	Category
	•	Subcategory

⸻

3. Pricing Data
	•	Includes:
	•	MAP Price (map_price)
	•	Purchase Price
	•	Used for identifying pricing violations

⸻

4. Promotion Data
	•	Seasonal promotion details (Q1–Q4)
	•	Includes various promotion types:
	•	Percentage discounts
	•	Fixed discounts
	•	Bundle offers

⸻

5. Seller Mapping
	•	Maps sellers to homologated (standardized) seller identifiers
	•	Enables seller-level compliance tracking

⸻

Notes
	•	The dataset provided is a sample (subset) of a larger dataset used during development
	•	Data has been curated to include both compliant and violation scenarios
	•	Additional edge cases (missing values, boundary conditions) are included to simulate real-world complexity
