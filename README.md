# South Africa Cadastral Parcels & Erf Lookup MCP

Connect your AI assistant (Claude, ChatGPT, Cursor) to [BumiAtlas](https://bumiatlas.com) for South African land research through the Model Context Protocol (MCP).

This listing is a focused entry point for:

- All ~9.1M surveyed parcels from the Chief Surveyor-General's national cadastre: erven, farm portions, parent farms, agricultural holdings and public places
- Parcel lookup by number and registration region (`erf 13583 East London`, `portion 11 of 930 Cape`), parent farm name, SG key, or coordinates
- CSG label (`RE/13583`), deed diagram, survey record and sectional title references, status codes and computed area
- Satellite and street map images of a parcel and its neighbours, labelled by CSG label

Parcels have no owner, title deed or value: the cadastre is surveyed boundaries only.

## Connect

```
https://bumiatlas.com/mcp/southafrica
```

Add it as a custom connector in any MCP client and sign in with Google. Tools, examples and data notes: [bumiatlas.com/mcp-docs/southafrica](https://bumiatlas.com/mcp-docs/southafrica).

- **Claude:** Settings → Connectors → Add custom connector, paste the URL, then Connect.
- **ChatGPT:** Settings → Apps & Connectors → Advanced → Developer mode, then Create with the URL and OAuth authentication.

## Tools

| Tool | Description |
|---|---|
| `ZA_parcel_search` | Find parcels by number and region, farm name, PRCL_KEY or SG id, or `latitude, longitude`; each result is the whole record, the boundary as GeoJSON on request |
| `ZA_parcel_image` | Satellite or street map image of a parcel or point, with every parcel in view outlined and labelled with its CSG label |

## Example prompts

- *"Which parcel is at -33.9249, 18.4241?"*
- *"Look up erf 13583 East London and show it on satellite imagery."*
- *"Find portion 11 of farm 930 in the Cape region."*
- *"Which parent farms are called Waterval?"*

## Data source

Cadastre © Chief Surveyor-General, South Africa, via the DFFE geoportal. A copy of public data for research, not a legal land record.
