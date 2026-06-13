# weather-routing-hires-land-data

Prebuilt high-resolution land edge index files for [signalk-weather-routing](https://github.com/kristianwiklund/signalk-weather-routing).

## Contents

| File | Size (gzipped) | Description |
|---|---|---|
| `edge-index.bin.gz` | 22 MB | Land edge index, GSHHG f-tier (full resolution), 179,837 polygons |
| `dilated-edge-index.bin.gz` | 75 MB | Same data dilated by 0.5 NM and union-merged to 16,802 polygons |

## Source data

Built from [GSHHG](https://www.soest.hawaii.edu/pwessel/gshhg/) (Global Self-consistent, Hierarchical, High-resolution Geography Database) version 2.3.7, full resolution (`f`) tier.

## Format

Binary edge-index format consumed directly by the signalk-weather-routing land avoidance engine. Files are gzip-compressed.

## License

GSHHG is distributed under the [LGPL](https://www.gnu.org/licenses/lgpl-3.0.html). These derived index files carry the same license.
