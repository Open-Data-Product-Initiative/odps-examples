# How Do I Define and Reuse a Payment Gateway in ODPS?

ODPS v4.0 allows you to modularly define payment gateways and reuse them across multiple pricing plans. This makes your data product metadata more maintainable and enables dynamic pricing automation.

---

## Step-by-Step Guide

### 1. Define Payment Gateways Inline

Declare one or more payment gateway configurations under the `paymentGateways` object.

```yaml
paymentGateways:
  default:
    description:
      en: Stripe-based API payment gateway
    type: Stripe
    version: 1
    reference: 'https://docs.stripe.com/'
    spec: |
      stripe.createCheckoutSession({
        amount: 4999,
        currency: 'usd',
        success_url: 'https://your-platform.com/success',
        cancel_url: 'https://your-platform.com/cancel'
      });

  agent:
    description:
      en: Payment gateway for AI agents
    type: Axio
    version: 1
    reference: 'https://www.x402.org/'
    spec: |
      paymentMiddleware("0xYourAddress", {"/mcp-access": "$0.01"});
```

---

### 2. Reference the Gateway in a Pricing Plan

In the `pricingPlans` block, reuse the gateway by referencing its key with `$ref`.

```yaml
pricingPlans:
  declarative:
    en:
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
          - No prioritization in case of peaks
        notes: >-
          Shadow pricing only for internal visibility. No actual billing applied.
        paymentGateway:
          $ref: '#/paymentGateways/default'
        dataQuality:
          $ref: '#/dataQuality/default'
        SLA:
          $ref: '#/SLA/default'
        access:
          $ref: '#/dataAccess/API'
```

---

### 3. External Payment Gateway Profiles

You can also reference payment gateways from **external YAML files** instead of defining them inline. This is helpful when managing multiple products that share common billing infrastructure.

#### Example 1: Whole payment gateway map from an external file

```yaml
paymentGateways:
  $ref: 'https://example.org/gateways/all-packages.yaml'
```

#### Example 2: Individual profiles from different files

```yaml
paymentGateways:
  default:
    $ref: 'https://example.org/gateways/basic.yaml'
  premium:
    $ref: 'https://example.org/gateways/premium.yaml'
```

---

## Summary

- Gateways can be defined inline or in external YAML files.
- Refer to gateways via `$ref` from within your pricing plans.
- Enables separation of concerns and reuse across products or environments.


[BACK TO INDEX](https://github.com/Open-Data-Product-Initiative/odps-examples/blob/main/README.md)