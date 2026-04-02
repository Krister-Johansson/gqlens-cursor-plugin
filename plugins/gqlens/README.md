# GQLens

GraphQL schema intelligence MCP server for Cursor.

## What it does

GQLens connects to your GraphQL endpoints, introspects the schema, and provides AI-powered tools for exploring and querying it — directly from your editor.

## Tools

| Tool | Description |
|------|-------------|
| `graphql_list_sources` | List all configured GraphQL sources for your organization |
| `graphql_schema_summary` | High-level overview: root operations, type counts, top types, and domain clusters |
| `graphql_search` | Keyword and semantic search across all types and fields |
| `graphql_list_types` | Paginated list of all types, filterable by kind and prefix |
| `graphql_type_docs` | Full documentation for a single type: fields, arguments, descriptions, deprecation info |
| `graphql_path_builder` | Traverse the schema graph from a root operation to a target type |
| `graphql_generate_examples` | Generate a minimal GraphQL operation template for a named root field |
| `graphql_validate_query` | Validate a GraphQL query string against the schema |

## Authentication

GQLens requires authentication via OAuth. When Cursor connects to the MCP server, it will automatically trigger the OAuth flow to authenticate with your GQLens account.

## Getting started

1. Install the GQLens plugin from the Cursor Marketplace
2. The MCP server will be added automatically
3. Authenticate when prompted
4. Start exploring your GraphQL schemas from Cursor

## Recommended workflow

1. **Understand the question** -- Identify what you want (e.g. "get assets for a user")
2. **Search first** -- Call `graphql_search` with keywords. This returns candidate groups, each representing a different domain/subgraph path to the data
3. **Present alternatives** -- If there are 2+ groups with strong or moderate intent match, compare the different approaches
4. **Drill into types** -- Call `graphql_type_docs` on the chosen approach's types to see fields, arguments, and descriptions
5. **Build the query** -- Call `graphql_generate_examples` for a starter template, or write the query yourself based on the type docs
6. **Validate** -- Call `graphql_validate_query` to check the query against the schema

For broad exploration, start with `graphql_schema_summary` to see the domain clusters, then use `graphql_list_types` with a prefix filter.

## Links

- [GQLens](https://gqlens.com)
- [Documentation](https://gqlens.com/docs)
