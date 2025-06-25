# How do I specify access roles or visibility rules?

In the **Open Data Product Specification (ODPS)**, access roles and visibility rules are declared using two key mechanisms:

---

### 1. **Visibility Setting (Required Field)**

The `visibility` field inside the `product.details` section defines the *overall access scope* of the data product.

```yaml
product:
  details:
    en:
      visibility: public  # or 'internal' or 'restricted'
```

- `public`: Accessible by anyone  
- `internal`: Limited to organization users or authenticated access  
- `restricted`: Subject to approval or contractual terms  

This field is mandatory and serves as the **first-level access control**.

---

### 2. **Access Profiles via `dataAccess` Block (Optional)**

You can define access methods and control policies using the `dataAccess` section, including API tokens, IP restrictions, or external access management platforms.

```yaml
dataAccess:
  API:
    description:
      en: Authenticated API access
    type: REST
    authenticationMethod: OAuth
```

This structure allows finer-grained **role- or org-based access restrictions** to be encoded declaratively.

---

### Summary

- Use `visibility` for high-level exposure settings (mandatory).
- Use `dataAccess` to declare role-based access control logic (optional).
- For monetized or SLA-bound products, pair with `pricingPlans`, `license`, and `contract` for policy enforcement.

[BACK TO INDEX](https://github.com/Open-Data-Product-Initiative/odps-examples/blob/main/README.md)
