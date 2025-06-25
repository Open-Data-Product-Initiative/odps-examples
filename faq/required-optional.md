# What are the required and optional sections in ODPS?

The **Open Data Product Specification (ODPS)** defines a YAML-based standard to describe interoperable, AI-friendly, and monetizable data products. This guide lists the **required** sections only, based on [ODPS v4.0](https://opendataproducts.org/v4.0/schema/odps.yaml).

---

## Required Sections

To comply with the ODPS schema, the following **minimum structure is required**:

```yaml
schema: https://opendataproducts.org/v4.0/schema/odps.yaml
version: 4.0

product:
  details:
    en:
      name: City Bike Stations
      productID: citybike-stations-001
      valueProposition: Real-time bike station data for smarter travel apps.
      description: Public data about station locations and availability in real-time.
      visibility: public
```

### Required Elements:

| Field                 | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| `schema`              | Points to the official ODPS schema version being used.                     |
| `version`             | Declares the version of the ODPS document (not schema).                    |
| `product.details.en`  | At least one language block (`en`, `fi`, `ar`, etc.) is mandatory.         |
| → `name`              | The name of the data product.                                               |
| → `productID`         | A unique, machine-readable identifier.                                     |
| → `valueProposition`  | The business or functional value for the consumer.                          |
| → `description`       | Human-readable explanation of the data product.                            |
| → `visibility`        | Visibility level: `public`, `internal`, or `restricted`.                   |

---

This structure is the **minimum required** to produce a valid ODPS YAML file. All other aspects are optional. 

---

## Summary

| Section                  | Required |
|--------------------------|----------|
| `schema`                 | ✅       |
| `version`                | ✅       |
| `product.details.en`     | ✅       |
| → `name`                 | ✅       |
| → `productID`            | ✅       |
| → `valueProposition`     | ✅       |
| → `description`          | ✅       |
| → `visibility`           | ✅       |


👉 [Download the minimal ODPS YAML used in this example](yaml/minimal)
