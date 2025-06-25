# 📄 How do I define a contract for my data product?

Defining a contract in ODPS ensures clarity about the agreement between the data holder and data user. You can define this either by pointing to an external contract file or writing the contract inline using YAML. Currently supported options: ODCS and DCS.

---

## 🧩 Structure of the contract element

The contract is defined under the `product` section using the following fields:

```yaml
product:
  contract:
    id: 02323M123  
    type: ODCS 
    contractVersion: 2.2.2
    contractURL: https://demo.datamesh-manager.com/demo834016807886/dataproducts/9bd53b1b-b51e-41a8-a757-4d33b4cde460
```

### Key fields explained

- **id**: A unique identifier for the contract. In this case: `02323M123`.
- **type**: Contract standard. Example uses `ODCS` (Open Data Contract Standard).
- **contractVersion**: Defines the version of the contract standard, not the actual contract instance.
- **contractURL**: A direct link to a contract hosted in a contract management system.

This method keeps your ODPS file light and points to the latest managed version of your contract.

---

## Inline contract definition

If you don’t want to link out, you can include the contract directly inside your ODPS file using the `spec` field:

```yaml
product:
  contract:
    type: ODCS 
    contractVersion: 2.2.2
    spec:
      # What's this data contract about?
      domain: seller # Domain
      dataProduct: my quantum # Data product name
      version: 1.1.0 # Version (follows semantic versioning)
      status: active
      id: 53581432-6c55-4ba2-a65f-72344a91553a

      # Lots of information
      description:
        purpose: Views built on top of the seller tables.
        limitations: Data based on seller perspective, no buyer information
        usage: Predict sales over time
        authoritativeDefinitions:
          - type: privacy-statement
            url: https://example.com/gdpr.pdf
      tenant: ClimateQuantumInc
      ...
```

This approach is useful when version control or portability matters more than using external systems.

---

## Summary

Use `contractURL` to point to managed contracts.  
Use `spec` for inline definitions when external services are unavailable or impractical.

👉 You can find the [full example YAML here](yaml/contract.yml)

[BACK TO INDEX](https://github.com/Open-Data-Product-Initiative/odps-examples/blob/main/README.md)
