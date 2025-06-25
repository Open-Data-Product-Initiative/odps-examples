# How Do I Define Related Products and Use Cases in ODPS?

ODPS v4.0 allows data product metadata to be enriched with **real-world use cases** and **recommendations for related data products**. This enhances discoverability and showcases how your data can deliver value.

---

## Step-by-Step Guide

### 1. Define Use Cases

Each use case explains **how the data product is used in practice**. This is useful for storytelling, adoption, and demonstrating business value.

```yaml
useCases:
  - useCase:
      useCaseTitle: Build attractive and lucrative petstore!
      useCaseDescription: Use case description how successful petstore chain was established in Abu Dhabi
      useCaseURL: https://marketplace.com/usecase1
```

- `useCaseTitle`: A short, attention-grabbing title.
- `useCaseDescription`: Summary of the impact or outcome achieved.
- `useCaseURL`: Link to a product spec, full story, blog, or customer reference.

---

### 2. Recommend Related Data Products

Use `recommendedDataProducts` to **suggest other useful data products** that complement this one.

```yaml
recommendedDataProducts:
  - https://marketplace.com/dataproduct.yaml
  - https://marketplace.com/dataproduct-another.yaml
```

These could be:
- Data products from the same provider
- Datasets used in similar solutions
- Bundled or follow-on products

---

## Summary

- Use `useCases` to demonstrate **value realization**.
- Use `recommendedDataProducts` to support **cross-selling, bundling**, or AI-assisted discovery.

[BACK TO INDEX](https://github.com/Open-Data-Product-Initiative/odps-examples/blob/main/README.md)