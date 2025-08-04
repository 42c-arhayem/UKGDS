# UKGDS Data Catalogue Metadata API

This repository contains the OpenAPI specification for the UK Government Digital Service (GDS) Data Catalogue Metadata API.

## Overview

The Data Catalogue Metadata API allows you to search, create, update and delete metadata records about data assets published in any data catalogue that implements the [data-catalogue-metadata JSON schema](https://co-cddo.github.io/data-catalogue-metadata/schema).

This JSON schema is based on the [Data Catalog Vocabulary (DCAT) - Version 3](https://www.w3.org/TR/vocab-dcat-3/).

An example of a data catalogue implementing this schema is the [CDDO Data Marketplace](https://datamarketplace.gov.uk).

## Files

- `metadata_management_api.yaml` - Main OpenAPI 3.0.0 specification
- `bundled_openapi_spec.json` - Bundled JSON version of the specification

## API Features

### Cataloged Resources
- Search and query data assets
- Filter by title, keywords, and supplier identifier

### Datasets
- Create, retrieve, update, and delete dataset resources
- Support for JSON Merge Patch updates
- Comprehensive validation and error handling

### Data Services
- Manage data service resources
- API endpoint management
- Dataset relationship tracking

## Security

The API uses OAuth 2.0 Client Credentials flow with the following scopes:
- `discover` - Discover data assets in the catalogue
- `publish` - Publish data assets to the catalogue  
- `delete` - Remove data assets from the catalogue

## Environments

- **Sandbox**: `https://api.sandbox.datamarketplace.gov.uk/v1`
- **Production**: `https://api.datamarketplace.gov.uk/v1`

## CI/CD

This repository includes GitHub Actions workflows for:
- OpenAPI specification validation
- Security scanning with 42Crunch
- Automated quality gates

## Contributing

Please ensure all changes to the OpenAPI specification are validated before committing.

## License

This project is licensed under the terms specified by UK Government Digital Service.
