# PANGAEA

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
