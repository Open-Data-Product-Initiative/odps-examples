# How Do I Assign SLAs to Pricing Plans in ODPS?

In ODPS v4.0, **Service Level Agreements (SLAs)** can be assigned to specific pricing plans by referencing named SLA packages. This modular design helps define different levels of availability, response time, and data refresh frequency — directly tied to the chosen pricing tier.

---

## SLA can be defined with 11 standardized dimensions

| SLA Dimension  | Description | 
|---|---|
| **latency** | minimal amount of time before getting any response. |
| **uptime** | Uptime is a measure of system reliability, expressed as the percentage of time a machine, typically a computer, has been working and available. See more https://uptime.is/. |
| **responseTime** | amount of time to process external request. |
| **errorRate** | Maximum tolerated errors in data, percentage. |
| **endOfSupport** | The date at which your product will not have support anymore. |
| **endOfLife** | The date at which your product will not be available anymore. No support, no access. |
| **updateFrequency** | how often data is updates. |
| **timeToDetect** | How fast can you detect a problem? |
| **timeToNotify** | Once you see a problem, how much time do you need to notify your users? |
| **timeToRepair** | How long do you need to fix the issue once it is detected? |
| **emailResponseTime** | How long do you need to respond to email support requests? |


--- 

## Step-by-Step Guide

### 1. Define SLA Packages

Declare the SLA packages under the `SLA` object using unique keys like `default` and `premium`.

- `objective` Target level to be achieved for the dimension (e.g., 99).
- `unit` Measurement unit for the SLA objective. If "date" is used, format should be dd/mm/yyyy.

```yaml
SLA:
  declarative:
    default:
        name:
            en: The Basic SLA
        description:
            en: The basic SLA package
        dimensions:
        - dimension: uptime
            displaytitle:
                en: Uptime
            objective: 90
            unit: percent
        - dimension: responseTime
            objective: 200
            unit: milliseconds
        - dimension: updateFrequency
            objective: 30
            unit: minutes

    premium:
        name:
            en: The Premium SLA
        description:
            en: The Premium SLA package
        dimensions:
        - dimension: uptime
            displaytitle:
                en: Uptime
            objective: 99
            unit: percent
        - dimension: responseTime
            objective: 100
            unit: milliseconds
        - dimension: updateFrequency
            objective: 5
            unit: minutes
```

---

### 2. Reference the SLA from the Pricing Plan

In your `pricingPlans`, use the `$ref` to point to the appropriate SLA package.

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

## Summary

- Define SLA sets under the `SLA` section.
- Reference them by name (e.g., `default`, `premium`) using `$ref` from within each pricing plan.
- This approach provides clarity, reuse, and machine-readability in data product metadata.

