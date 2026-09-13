# Data notes

## GRID3 Nigeria LGA Boundary Dataset

- Source: https://data.grid3.org/datasets/GRID3::grid3-nga-operational-lga-boundaries/about
- Downloaded: 7th September, 2026
- Layer: "grid3_nga_boundary_vacclgas"
- 774 features, multipolygons
- Columns
    - FID: 519
    - globalid: 7ce9323f-9136-4314-8197-32efdb87e27e
    - uniq_id: 28549
    - timestamp: 2019-08-09T00:00:00.000Z
    - editor: nuraddeen.isah
    - lganame: Katsina-Ala
    - lgacode: 7009
    - statename: Benue
    - statecode: BE
    - source: GRID
    - amapcode: NIE BNS KAL
- Nulls:  No nulls found in "lganame", "statename", or "lgacode".
- Coverage: The dataset contains Nigerian LGA boundaries and includes Katsina-Ala LGA in Benue State.

## OSM roads, extracted via Overpass Turbo

- Query: "highway=*" within Katsina-Ala extent
- https://overpass-turbo.eu/s/2wro
- Extracted: 13 September 2026
- 5 features, lines
- Key columns: "highway", "name", "ref", "surface"
- Some features have no "ref" or "surface" value.
- Coverage/extent should be treated as limited to the roads returned by the query; unnamed roads were excluded because the query used "name".

## OSM waterways, extracted via Overpass Turbo

- Query: "waterway=*" with "name=*" within Katsina-Ala extent
- Extracted: 13 September 2026
- 7 features, lines
- Key columns: "waterway", "name", "intermittent", "source"
- Most features have no "intermittent" or "source" value.
- Named waterways are represented as LineStrings; coverage is limited to waterways returned by the OSM query.

## OSM places/settlements

- Source: OpenStreetMap, extracted via Overpass Turbo
- Query: "node["place"]" within Katsina-Ala extent
- https://overpass-turbo.eu/s/2wrm
- Extracted: 13 September 2026
- Features: 21
- Geometry: Point
- Key columns: "place"
- Other column: "@id" (OSM feature identifier)
- Missing values: No missing values in "place" or "@id".
- Observation: The dataset contains mapped OSM places/settlements within the study area. Coverage depends on what has been mapped in OpenStreetMap, so unmapped settlements will not appear.
