# Dotmatics GraphQL API

## Description

Dotmatics provides a GraphQL API as part of its Luma Scientific Intelligence Platform, alongside REST and JDBC interfaces. The GraphQL layer enables flexible, query-driven access to scientific data managed across the Dotmatics product suite — including compound and sample registries, study definitions, assay results, screening workflows, ELN records, sequences, and chemical structures.

The API supports pharma and biotech R&D organizations in querying experimental data, navigating relationships between entities (e.g., compounds to batches, protocols to results), and integrating with external LIMS, data warehouses, and BI tools.

## Endpoint

```
https://api.dotmatics.com/graphql
```

Authentication is via OAuth 2.0 bearer token issued through the Dotmatics Luma platform identity provider. Tenant-specific subdomains may apply (e.g., `https://{tenant}.dotmatics.com/graphql`).

## Documentation

- Platform overview: https://www.dotmatics.com/capabilities/scientific-data-search
- What's new / release notes: https://www.dotmatics.com/whats-new
- GitHub organization (TypeScript codegen and OpenAPI references): https://github.com/dotmatics
- TypeScript client codegen: https://github.com/dotmatics/openapi-typescript-codegen

## Products Covered

The GraphQL schema spans data from multiple Dotmatics products:

- **Luma** — Scientific intelligence platform; primary API surface
- **Studies** — HTS, HCS, and DMPK screening study management
- **Bioregister** — Compound and biological entity registration
- **ELN** — Electronic Lab Notebook entries, experiments, reactions
- **Vortex** — Data visualization and analysis
- **Geneious** — Sequence and bioinformatics data
- **SnapGene** — Plasmid and DNA construct records
- **Protein Metrics** — Proteomics and mass spec results

## Notes

- The GraphQL schema below is a conceptual model derived from the Dotmatics data domain. Dotmatics has not published a standalone public GraphQL introspection endpoint or SDL at the time of writing.
- Field names and type names follow conventions observable from Dotmatics REST API resources, documentation, and the TypeScript codegen repository.
- Consumers should confirm exact field names, nullability, and available mutations against their tenant's schema via introspection once access is provisioned.
