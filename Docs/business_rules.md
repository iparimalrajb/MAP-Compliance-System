# Business Rules – MAP Compliance System

This document defines the rules used to identify pricing violations in the MAP Compliance Monitoring System.

---

## Rule 1: MAP Violation

**Condition:**
- Advertised Price < MAP Price  

**Action:**
- Mark as `VIOLATION`

**Business Impact:**
Violates brand pricing policy and can lead to price erosion across marketplaces.

---

## Rule 2: Promotion Violation

**Condition:**
- Promotion is active for the given time period (e.g., Q1 / Q2 / Q3 / Q4)  
- Promotion Price is available  
- Advertised Price < Promotion Price  

**Action:**
- Mark as `VIOLATION`

**Business Impact:**
Undercuts promotional pricing strategy and creates unfair competition.

---

## Rule Priority

If multiple rules are triggered:
1. Promotion Violation takes priority  
2. MAP Violation is applied otherwise  

---

## Edge Case Handling

- Missing MAP Price → Skip MAP validation  
- Missing Promotion Price → Skip promotion validation

---

## Violation Levels

- **Level 1:** First-time violation → Violation Letter.
- **Level 2:** Repeated violation → Warning Letter.
- **Level 3:** Continuous violation → Suspension Letter for the affected category.

---