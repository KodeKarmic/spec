### FR-012: Create Project

## Persona Policy (Required)
- PrimaryPersona: SeniorDeveloper
- SecondaryPersonas: [TestEngineer]
- ExcludedPersonas: [SolutionArchitect]
- DeliveryMode: MVP
- ComplexityBudget: Low

## Output Constraints (Required)
- MustInclude:
  - Input validation + deterministic error codes
  - Unit tests for happy/negative/boundary
- MustAvoid:
  - Plugin architecture
  - Policy engine / RBAC matrix
  - Event-driven workflow
