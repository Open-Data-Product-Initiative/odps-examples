# How does ODPS support AI agent consumption?

ODPS (Open Data Product Specification) supports AI agent consumption by making data products machine-readable, self-describing, and agent-accessible by design. Here’s how:

### Structured Metadata for Agents

ODPS organizes metadata in a standardized YAML format, enabling AI agents to interpret key information like schemas, access methods, pricing plans, and SLAs without human involvement. This allows autonomous systems to assess, compare, and select datasets.

### Referencing and Reusability

Modular components (e.g., dataAccess, license, dataQuality, pricingPlans) can be reused and referenced. AI agents can follow these links to build a complete picture of a product’s structure and obligations [1].

### Alignment with MCP (Model Context Protocol)

ODPS complements MCP, which allows AI agents to dynamically explore, query, and consume data products. ODPS provides the "what" (declaration), while MCP handles the "how" (runtime interaction) [1].

### Support for AI-Native Experiences

ODPS is designed for both human and non-human (AI) consumers. It ensures agents can identify product value, assess governance constraints, and execute data access workflows programmatically.

##  How ODPS v4 actively supports AI agent consumption

**1. Modular Referencing & Discoverability**

ODPS v4 introduces first-class references (e.g., $ref: '#/dataAccess/API') for key sections—like dataAccess, dataQuality, SLA, pricingPlans, and paymentGateways. This makes the metadata lightweight, discoverable, and self-contained for agents to parse easily.

**2. AI-Aware Interfaces & Access Design**

You can define specialized “AI-agent” access methods under dataAccess—including vector embeddings, agent-specific ports, and schema descriptions. Agents can query #/product/dataAccess/YourAgentMethod via the registry to locate agent-friendly endpoints
blog.opendataproducts.org.

**3. Pricing & Provisioning as Code**

ODPS supports “pricingPlans” with $ref to shared profiles, including agent-specific plans. This enables AI agents to:

- Discover suitable pricing tiers
- Automatically calculate costs
- Execute provisioning or payment workflows (with paymentGateways spec)

**4. Automated Quality & SLA Checks**

AI consumers rely on data reliability. ODPS v4 supports:

- Data Quality as Code: structured executable rules for dimensions like accuracy, completeness, and timeliness
- SLA as Code: machine-verifiable uptime & latency thresholds
- Both can be referenced in the product spec or external catalogs, so agents can validate promised vs actual performance

**5. Full Autonomous Agent Consumption Lifecycle**

According to Moilanen et al., ODPS enables the entire AI agent lifecycle—from discovery and evaluation through purchase, onboarding, and continuous monitoring—without human involvement. Features like metadata clarity, contractability, pricing-as-code, DQ/SLA enforcement, and even consumption tracking are all supported


In short, ODPS + MCP creates the foundation for an AI-native data economy.

