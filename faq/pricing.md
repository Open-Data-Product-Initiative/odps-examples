# How do I define pricing plans?

ODPS allows you to describe flexible, tiered pricing plans for your data product. These plans define cost, billing rules, usage limits, and links to service-level agreements (SLAs), data quality (DQ) expectations, access types, and payment gateways.

The 12 pricing plans enabled by ODPS are meticulously defined through an in-depth analysis of pricing models applied across more than 300 data products.

| Pricing plan   | Description | 
|---|---|
| **Recurring time period based** | In the simplest terms, recurring payments (also known as subscription payments, automatic payments, or recurring billing) take place when customers authorize a merchant to charge them repeatedly for goods or services on a prearranged schedule.|
| **One time payments plans** | One Time Fee Revenue Model is a business model that generates revenue through a single payment for perpetual product use or service access. The One Time Fee Revenue Model is a fundamental concept in the world of small businesses and entrepreneurship. |
| **Pay-as-you-go plans** | The Pay As You Go Plan is a flexible alternative to a monthly plan. Instead of paying a recurring monthly charge, you buy credits as needed. |
| **Revenue sharing plans** | Revenue sharing is a performance-based income model that involves sharing business profits or losses among participating partners. Revenue sharing is a profit-sharing system that ensures all parties involved are compensated for their contribution to the business. |
| **Data volume plan** | Volume pricing is a pricing strategy in which an item's price per unit decreases as the purchase quantity increases. |
| **Trial** | A free trial pricing strategy offers target customers a chance to try your product for free for a limited time. It is a sales promotion technique that uses the product to market itself.  |
| **Dynamic pricing** | Dynamic pricing is a pricing strategy that applies variable prices instead of fixed prices. Instead of deciding on a set price for a season, retailers can update their prices multiple times per day to capitalize on the ever-changing market. |
| **Pay what you want plans** |  Also known as PWYW pricing, is a pricing strategy in which buyers pay the desired price for a particular product, commodity, or service. The approach may sometimes lead to the value of zero. Following the buyer's guidance, one can set a suggested price and a minimum price. |
| **Freemium** |  A type of business model that offers basic features of a product or service to users at no cost and charges a premium for supplemental or advanced features. |
| **Open data** | Access to open data is expected to be free of cost, but in some cases it is also possible to collect fees to cover costs of the service.  |
| **Value-based** | Value-based pricing is a strategy of setting prices primarily based on a consumer's perceived value of a product or service. Value-based pricing is customer-focused, meaning companies base their pricing on how much the customer believes a product is worth. Often worth to provide customer a value simulator to see expected value gains and possibly set the price based on that. Pricing would be customized per customer. |
| **On Request** | Access to data product is given only on request. Often provider expects customer to meet provider first. In the discussions conditions, pricing etc are agreed. |

The Pricing object is general in nature and should be enough for common (80%) use cases. You can make extensions to the standard with "x-" mechanism in order to fulfill any industry specific needs. 

---

## Structure of `pricingPlans`

In the example below, the `pricingPlans` section is defined under:

```yaml
product:
  pricingPlans:
    declarative:
      en:
```

Each plan includes:

- `name`: The label of the plan.
- `priceCurrency` and `price`: What the user pays.
- `billingDuration` and `unit`: The frequency and nature of billing.
- `maxTransactionQuantity`: Usage cap, often by API queries or downloads.
- `offering`: A list describing what the user gets.
- `notes`: Internal-only fields such as shadow pricing.

### Example snippet:

```yaml
- name: Basic Reader
  priceCurrency: USD
  price: 0
  billingDuration: month
  unit: recurring
  maxTransactionQuantity: 100
  offering:
    - Standard access to event metadata
    - Up to 100 SQL queries per month
    - Shared SLA (best-effort availability)
```

This defines a free tier ("Basic Reader") with a usage cap of 100 queries/month and basic service expectations.

---

## Linking to SLA, DQ, Access and Payment Gateway

Each pricing plan can reference reusable components defined elsewhere in the ODPS YAML:

```yaml
paymentGateway:
  $ref: '#/paymentGateways/default'
dataQuality:
  $ref: '#/dataQuality/default'
SLA:
  $ref: '#/SLA/default'
access:
  $ref: '#/dataAccess/API'
```

These `$ref` links avoid duplication and centralize updates.

---

## Multi-Tier Pricing Example

Here's a higher tier with a fee and better terms:

```yaml

- name: High Volume Access
  priceCurrency: USD
  price: 2000
  billingDuration: month
  unit: recurring
  maxTransactionQuantity: 500000
  offering:
    - Dedicated API channel for bulk usage
    - Up to 500,000 SQL queries per month
    - Guaranteed SLA for availability and response time
  paymentGateway:
    $ref: '#/Product/paymentGateways/agent'
  dataQuality:
    $ref: '#/Product/dataQuality/premium'
  SLA:
    $ref: '#/Product/SLA/premium'
  access:
    $ref: '#/Product/dataAccess/Agent'

```

The plan connects to premium SLA and data quality profiles and uses a dedicated AI-agent payment gateway.

---

## Summary

ODPS lets you define pricing plans that match your business model. You can:

- Offer free or premium tiers
- Reuse SLA, DQ, Access, and Payment configurations
- Apply shadow pricing for internal use
- Define billing rules clearly

📄 [View the full YAML example](yaml/pricing.yml)

[BACK TO INDEX](https://github.com/Open-Data-Product-Initiative/odps-examples/blob/main/README.md)