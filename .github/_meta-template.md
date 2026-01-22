## Persona Policy (Required)
- PrimaryPersona: <one of allowed values>
- SecondaryPersonas: [<0-3 personas>]
- ExcludedPersonas: [<any personas that must NOT influence the output>]
- DeliveryMode: MVP | Standard | Enterprise
- ComplexityBudget: Low | Medium | High

## Output Constraints (Required)
- MustInclude:
  - <e.g., traceability updates, tests, ADR, etc.>
- MustAvoid:
  - <e.g., plugin architecture, multi-tenant RBAC, event bus, etc. unless specified>
