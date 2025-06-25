
# How to Validate an ODPS YAML File

This guide explains how to validate your Open Data Product Specification (ODPS) YAML files for both basic syntax and compliance with the official ODPS schema.

---

## 1. 🔍 Validate YAML Syntax

Before ODPS-specific validation, ensure the file is valid YAML:

### Online Tools
- **[YAMLlint](https://www.yamllint.com/)** – Paste your YAML and check for syntax errors.
- **[CodeBeautify YAML Validator](https://codebeautify.org/yaml-validator)** – Supports uploading files or validating from a URL.

### Command Line Tool
Use `yq` to test:
```bash
yq eval myfile.yaml > /dev/null && echo "Valid YAML"
```

More info on `yq`: [StackOverflow](https://stackoverflow.com/questions/75920947/how-to-validate-yaml-using-yq)

---

## 2. Validate Against ODPS Schema

To confirm that your YAML follows ODPS rules:

### Use the Schema URL

Make sure your YAML includes:
```yaml
schema: https://opendataproducts.org/v3.1/schema/odps.yaml
```
Or for ODPS v4:
```yaml
schema: https://opendataproducts.org/4.0/odps.yaml
```

### Validation Tools

- **VSCode / VSCodium**: Enable RedHat YAML schema validation (auto detects based on `schema:` field).
- **yamale**: CLI tool to validate YAML against schemas.
- Ensure any `$ref:` links in your YAML resolve properly to other YAML structures (either inline or external URLs).

---

## Tips
- Follow the [ODPS Dev Page](https://opendataproducts.org/dev/) for the latest schema definitions and best practices.
- Modular YAML? Validate each referenced file separately if needed.

[BACK TO INDEX](https://github.com/Open-Data-Product-Initiative/odps-examples/blob/main/README.md)
