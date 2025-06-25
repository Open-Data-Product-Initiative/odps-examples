# How do I define metadata for my data product?

## 🧭 Introduction

The Open Data Product Specification (ODPS) v4.0 is a machine-readable metadata standard for defining data products. It is structured to support discoverability, interoperability, monetization, compliance, and AI-native usage.

---

## Main Objects and Their Purpose

### 1. `schema` & `version`
- **Purpose**: Identify the ODPS schema in use and the version of this metadata document.

### 2. `product`
Root element containing all data product metadata.

#### a. `contract`
- Defining data contract to use (e.g., DCS, ODCS).

#### b. `details`
- Human-readable metadata including:
  - `name`: Data product name
  - `productID`: Unique identifier
  - `valueProposition`: What value it offers
  - `description`: What it contains
  - `visibility`: `public`, `internal`, or `restricted`
  - ...

#### c. `pricingPlans`
- Pricing models: Free, subscription, usage-based...
- Supports linking to SLAs, access rules, payment gateways, and quality guarantees

#### d. `SLA`
- Defines performance objectives such as:
  - Uptime
  - Latency
  - Update frequency
  - ...

#### e. `dataQuality`
- Measures of data fitness:
  - Accuracy
  - Completeness
  - Timeliness
  - ...

#### f. `dataAccess`
- Technical access information:
  - Protocols
  - Endpoints
  - Authentication methods

#### g. `paymentGateways`
- Metadata for monetization mechanisms:

#### h. `license`
- Legal license under which the data is provided (e.g., SPDX ID or custom license)

#### i. `dataHolder`
- Contact and responsibility metadata for the organization or person maintaining the product

[BACK TO INDEX](https://github.com/Open-Data-Product-Initiative/odps-examples/blob/main/README.md)

