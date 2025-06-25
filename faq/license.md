# How Do I Declare a License Using ODPS?

ODPS v4.0 provides two methods to declare licensing information for your data product. You can either **link to an external license definition** or **embed a detailed inline license object**.

---

## Option 1: Reference an External License

Use `$ref` to link your data product to a hosted license definition.

```yaml
license:
  $ref: 'https://example.org/licenses/default'
```

This is useful when using standardized or reusable licenses such as Creative Commons or your own externally hosted license.

---

## Option 2: Inline License Declaration

You can provide a detailed license directly within the ODPS YAML file.

```yaml
license:
  en:
    scope:
      definition: The purpose of this license is to determine the terms and conditions applicable to the licensing of the data product, whereby Data Holder grants Data User the right to use the data.
      restrictions: Data User agrees not to, directly or indirectly, participate in the unauthorized use, disclosure or conversion of any confidential information.
      geographicalArea:
        - EU
        - US
      permanent: false
      exclusive: false
      rights:
        - Reproduction
        - Display
        - Distribution
        - Adaptation
        - Reselling
        - Sublicensing
        - Transferring
    termination:
      noticePeriod: 90
      terminationConditions: After the expiry of the right of use, the product and its derivatives must be removed.
      continuityConditions: Expired license will automatically continue without written cancellation (termination) by Data Holder.
    governance:
      ownership: Mindmote Oy, a company specializing in pet industry insights, owns the license to its proprietary data product 'Pets of the Year'.
      damages: During the term of license, except for force majeure or reasons from the Data Holder, the Data User is required to comply strictly with the license. If the Data User wants to terminate the license early, it must pay a specified amount of liquidated damages.
      confidentiality: Data User agrees to maintain confidentiality concerning all technical (e.g., drawings, tables, formulas) and commercial (e.g., contract terms, prices) information obtained during the license.
      applicableLaws: This license shall be interpreted and enforced under Finnish law, including Copyright Act 404/1961.
      warranties: Data Holder provides no warranties, guarantees, or conditions. All liability for damages is disclaimed to the extent permitted by law.
      audit: Data Holder will cooperate with reasonable audit requests. Each party bears its own costs.
      forceMajeure: Obligations may be suspended due to uncontrollable events like strikes, wars, or natural disasters.
```
