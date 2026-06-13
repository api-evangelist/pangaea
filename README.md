# PANGAEA

PANGAEA is a data publisher and library for earth and environmental science, providing open access to geoscientific datasets including ocean data, climate records, sediment cores, and environmental measurements from scientific expeditions worldwide. With over 445,000 datasets, PANGAEA serves as a critical infrastructure for the earth science research community.

## APIs

This repository catalogs the following PANGAEA public APIs:

### Elasticsearch Search API
Full-text and faceted search across PANGAEA's datasets. Supports spatial bounding box queries, temporal filtering, topic classification, and author/campaign searches.

- Base URL: `https://ws.pangaea.de/es/pangaea/panmd/_search`
- Protocol: REST (Elasticsearch)
- Auth: None required

### OAI-PMH Metadata Harvesting API
OAI-PMH 2.0 compliant endpoint for systematic metadata harvesting. Supports JSON-LD, DataCite XML, Dublin Core XML, ISO 19115/19139, and DIF/FGDC formats.

- Base URL: `https://ws.pangaea.de/oai/provider`
- Protocol: OAI-PMH 2.0
- Auth: None required

### Data Download Service - Filter by DOI
Retrieve filtered tabular data from a specific PANGAEA dataset identified by its DOI, with support for column selection and value-range filtering.

- Base URL: `https://ws.pangaea.de/dds-fdp/rest/panquery`
- Protocol: REST
- Auth: None required

### Data Download Service - Filter by Geo/Parameters
Cross-dataset data retrieval filtered by geographic bounding box, temporal range, depth constraints, and PANGAEA parameter IDs.

- Base URL: `https://ws.pangaea.de/dds-fgp/rest/dwhquery`
- Protocol: REST
- Auth: None required

### Bathymetry WMS
OGC-compliant Web Map Service providing bathymetric map layers based on PANGAEA-collected ocean depth measurements.

- Base URL: `https://maps.awi.de/services/common/pangaea_bathymetry/wms`
- Protocol: OGC WMS
- Auth: None required

### Term Dictionary API
Query PANGAEA's controlled vocabulary for dataset classification topics, parameters, and methods.

- Base URL: `https://ws.pangaea.de/es/pangaea-terms/term/_search`
- Protocol: REST (Elasticsearch)
- Auth: None required

## Client Libraries

- **Python**: [pangaeapy](https://pypi.org/project/pangaeapy/) — `pip install pangaeapy`
- **R**: [pangaear](https://ropensci.github.io/pangaear/) — `install.packages("pangaear")`

## Pricing & Access

All PANGAEA APIs are free to use. PANGAEA is publicly funded by the Alfred Wegener Institute (AWI), MARUM (University of Bremen), and the Helmholtz Association. No API key or registration is required for public dataset access.

## Contact

- Technical: tech@pangaea.de
- Website: https://www.pangaea.de/
- Services: https://www.pangaea.de/about/services.php
- Wiki: https://wiki.pangaea.de/
