# How do I define data quality rules?

The Open Data Product Specification (ODPS) makes data quality (DQ) an explicit, structured component of any data product. You can define clear, measurable rules for different quality dimensions and attach them to pricing plans.

Let’s break it down with a real example.

## Where is data quality defined?

In the ODPS YAML, the `dataQuality` section holds the rules. Here's the starting structure:

```yaml
dataQuality:
  default:
    displaytitle:
      en: Complete Data Quality Set
    description:
      en: Includes all defined data quality dimensions.
    dimensions:
```

Each quality **dimension** is then defined with a name, description, and an objective value. For example:

```yaml
- dimension: accuracy
  displaytitle:
    en: Data Accuracy
  description:
    en: How well the data reflects the real-world entities or events it represents.
  objective: 95
  unit: percent
```

This means the data product should maintain **95% accuracy**.

## What kind of dimensions can I use?

Here are some dimensions defined in the example:

- **Accuracy**: Real-world representation
- **Completeness**: All required data attributes present
- **Conformity**: Adherence to syntax or schema
- **Consistency**: Uniform values across datasets
- **Coverage**: Extent of records present
- **Timeliness**: How current the data is
- **Validity**: Logical correctness
- **Uniqueness**: No duplicates

Each has a percentage objective. These act like contracts for data quality expectations.

## How do I use DQ in pricing plans?

Once you've defined DQ rules, you can reuse them via a `$ref`:

```yaml
dataQuality:
  $ref: '#/dataQuality/default'
```

This makes the `default` DQ package available to any pricing plan or product configuration. It avoids duplication and allows you to manage DQ rules in one place.

## Why does this matter?

ODPS helps shift quality from abstract claims to measurable commitments. This supports trust, comparisons, and automation.

👉 [Download the full ODPS YAML used in this example](yaml/dq.yml)
