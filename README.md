# VRF Web2 API Specifications
## API Documentation Links
- [VRF Web2 API SPECIFICATIONS (V1.0.0) - download HTML file and open locally in browser](https://github.com/vreff/VRF-Web2-API-Specifications/blob/main/index.html)
- [VRF Web2 API SPECIFICATIONS (V1.0.0) - PDF](https://github.com/vreff/VRF-Web2-API-Specifications/blob/main/API-Specs.pdf)
## Purpose
- Provide OpenAPI-compliant documentation for intended APIs that will interface with VRF Web2.
- Enable rapid iteration on APIs.
## Tooling
- This package uses `openapi-generator-cli` to produce html-compatible documents.
- API specifications are contained in `api.yaml`, and converted to the code in `index.html` by the cli tool.
- To regenerate the `index.html` file after changin `api.yaml`, do the following:
  - `npm install -g @openapitools/openapi-generator-cli`
  - `openapi-generator-cli version-manager set 5.4.0` -- the default version is not stable with html documents.
  - `openapi-generator-cli generate -g html2 -i api.yaml -o . -t ./htmlDocs2`
- For markdown docs:
  - `openapi-generator-cli generate -g markdown -i api.yaml -o ./markdown`

## Extra
- `htmlDocs2` templates folder vendored from: https://github.com/OpenAPITools/openapi-generator/tree/master/modules/openapi-generator/src/main/resources/htmlDocs2
