# ❓ What is ODPS, and why should I use it?

ODPS stands for **Open Data Product Specification**. It is an open standard for describing data products in a **machine-readable** way. ODPS brings clarity, structure, and interoperability to how data products are defined, published, and consumed.

You can think of ODPS like a blueprint for your data product — not just describing what data it contains, but how it can be accessed, under what license, at what price, with what quality and SLA guarantees, and more.

## Why was ODPS created?

Most data platforms treat data assets as raw, technical artifacts. But modern teams want to sell, share, and maintain **data products**. That shift demands a clear specification, similar to how APIs are described using OpenAPI.

ODPS does for data products what OpenAPI does for APIs.

## Key benefits

- Standardizes how data products are described across teams and platforms  
- Makes data products **self-describing** and **interoperable**  
- Allows automation of pricing, licensing, SLA, and quality enforcement  
- Helps humans and AI agents discover, understand, and consume data  
- Aligns with open data policies and monetization needs  

## Quick example

Here’s a simple ODPS product definition (just [YAML](yaml/minimal.yml)):

```yaml
schema: https://opendataproducts.org/v3.1/schema/odps.yaml
version: 3.1

product:
  details:
    en:
      name: City Bike Stations
      productID: citybike-stations-001
      valueProposition: Real-time bike station data for smarter travel apps.
      description: Public data about station locations and availability in real-time.
      visibility: public
```
This is just the start. You can add pricing, data access methods, contracts, and much more.

## Who maintains ODPS?

ODPS is a **Linux Foundation open standard**, with active adoption across the public sector, platforms, and enterprises. It is maintained by an open community and led by **Dr. Jarkko Moilanen**, its original author, and **Manfred Sorg**.

You can learn more and join the community at [opendataproducts.org](https://opendataproducts.org/).
