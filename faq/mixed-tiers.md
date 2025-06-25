# Can I Offer Free and Paid Tiers in the Same Product?

Yes, offering **both free and paid tiers** within the same data product is a widely used and recommended strategy. This approach is called **freemium tiered pricing**. It allows you to:

1. **Attract users with a free tier** – Lower barrier to entry, especially useful in open data and SaaS models.
2. **Upsell premium features** – Offer value-added features, higher API rate limits, fresher data, or analytics dashboards as part of paid tiers.
3. **Validate product-market fit** – Free users help test and provide feedback; conversions indicate monetization potential.
4. **Optimize for different personas** – Governments, students, and developers may stay on the free tier, while enterprises adopt premium plans.

In ODPS (Open Data Product Specification), this is supported under the `pricingPlans` section using a structure like:

```yaml
pricingPlans:
  free:
    declarative:
      en:
        planName: Free Tier
        description: Basic access with limited API calls
        price: 0
  pro:
    declarative:
      en:
        planName: Pro Tier
        description: Full access with support and SLA
        price: 99
```

This model is scalable and allows pricing to evolve over time based on usage patterns and demand.

📄 [View the full YAML example](yaml/pricing.yml)

[BACK TO INDEX](https://github.com/Open-Data-Product-Initiative/odps-examples/blob/main/README.md)