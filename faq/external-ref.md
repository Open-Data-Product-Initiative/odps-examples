
# Can I reference external YAML files?

**Yes! ODPS fully supports referencing external YAML files** for shared objects like SLA, Data Quality, Data Access, and Payment Gateways. This enables modular, maintainable, and scalable specifications — ideal for organizations managing many data products.



## Why reference external files?

Referencing external YAML files provides significant advantages, especially as your data product ecosystem scales:

- **Reuse across many products and plans**  
  Define once, apply across multiple products, pricing tiers, or even organizations in your ecosystem. No duplication means faster time-to-market for new offerings.

- **Centralized maintenance**  
  When SLAs, Data Quality packages, or Access definitions change (e.g., a new uptime target), you update the external file — and all products referencing it automatically align. This reduces manual effort and prevents inconsistencies.

- **Cleaner, simpler product specs**  
  Pricing plans can focus on what makes them unique (price, limits, offerings), while common service terms live elsewhere. This makes specs easier to read, validate, and govern.

- **Cross-team collaboration**  
  Teams managing SLAs or API access don’t need to touch individual product YAMLs. They publish shared specs that product owners simply consume via `$ref`.

- **Compliance and audit readiness**  
  External files let you version and document contractual terms (SLA, licensing, access) in a traceable, consistent manner — helping with audits, regulatory reviews, and internal governance.

- **Scalability of ecosystem**  
  When working across multiple business units, partners, or open data platforms, external definitions ensure everyone adheres to the same baseline terms without duplication or drift.

- **AI & automation friendly**  
  External structured files make it easier for AI agents, monitoring tools, or validation systems to consume, verify, or enforce policies programmatically.

---

## How to reference external YAML files

You can define **shared objects at the top level of your product spec** or in external files. 

### Example of defining shared objects via external files:

```yaml
SLA:
  $ref: 'https://example.com/odps-sla-definitions.yaml'

dataQuality:
  $ref: 'https://example.com/odps-dq-definitions.yaml'

paymentGateways:
  $ref: 'https://example.com/odps-gateways.yaml'

dataAccess:
  $ref: 'https://example.com/odps-access.yaml'
```

➡ **Note:** These are object-level references in your product specification — not direct parts of individual `pricingPlans`. The `pricingPlans` will reference these shared objects using internal or external `$ref`.


## Best practices

- Ensure external files are **publicly accessible or accessible to your processing tool**
- Use **stable URLs** or versioned files to avoid breaking changes
- Document what each external component provides
- Validate your spec to ensure all external `$ref` targets resolve correctly



## When to use external references

| When | Example |
|-------|---------|
| Shared SLA across multiple products | All city data APIs use the same `premium` SLA object |
| Shared data access definition | All products provide standard API endpoints from one spec |
| Shared gateways for billing consistency | All products route payments through the same provider |

