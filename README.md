# Resibre Repository Overview

Resilience AI Solution Private Limited (RAISPL) is launching Resibre platform for aiding better Disaster Risk Management across the globe. 

This repository provides an end‑to‑end pipeline for generating physical asset risk assets against different climate events. It offers a workflow via a simple Flask API so that end users can upload source data and retrieve results. 

The project has been built for creating a first version of a Disaster Management Plan (DMP).  It stitches together computer‑vision models and geospatial Artificial Intelligence tools to automate the following steps:

1. **Tile Generation** – Large TIFF images are split into fixed‑size tiles (512×512 pixels) so that they can be processed efficiently.
2. **Building Footprint Extraction** – A UNet segmentation model is used to detect building outlines within each tile, generating a GeoJSON of footprints.
3. **Roof Type Classification** – Each footprint is cropped from the original imagery and passed through an image classifier (Inception v3) to assign a roof type label.
4. **Physical Asset Risk Calculation** – Environmental layers (water bodies, elevation, NDVI, land cover, etc.) are combined with footprint attributes to assign an overall risk score.
5. **API Interface** – A Flask application exposes endpoints to trigger each stage individually or to run the entire pipeline end‑to‑end.


## License

[Apache LICENSE-2.0](https://www.apache.org/licenses/LICENSE-2.0)

RAISPL also offers a Enterprise version of this platform with support, security & Enterprise deployment for various sectors. Contact partnership@resilience360.ai for details.
