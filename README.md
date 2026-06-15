# weather-routing-hires-land-data

Prebuilt high-resolution land edge index files for [signalk-weather-routing](https://github.com/kristianwiklund/signalk-weather-routing).

## Download

The binary files are distributed as **release assets** (not committed to the repo) because they exceed GitHub's 100 MB file limit.

Download the latest files from the [releases page](https://github.com/kristianwiklund/weather-routing-hires-land-data/releases):

| File | Size | Description |
|---|---|---|
| `edge-index-hires.bin.gz` | ~87 MB | Land edge index, GSHHG f-tier (full resolution, ~100 m), 179,837 polygons |
| `dilated-edge-index-hires.bin.gz` | ~160 MB | Same data dilated by 0.5 NM and union-merged |

## Installation

Copy both files into the plugin's `data/` directory:

```bash
cp edge-index-hires.bin.gz dilated-edge-index-hires.bin.gz /path/to/signalk-weather-routing/data/
```

The plugin detects the files at startup and automatically switches to the high-resolution land index. The sidebar will show "(hires)" next to the Land overlay checkbox.

## Source data

Built from [GSHHG](https://www.soest.hawaii.edu/pwessel/gshhg/) (Global Self-consistent, Hierarchical, High-resolution Geography Database) version 2.3.7, full resolution (`f`) tier.

Build command:
```
python3 scripts/prepare-land-data.py -r f
```

## License

GSHHG is distributed under the [LGPL](https://www.gnu.org/licenses/lgpl-3.0.html). These derived index files carry the same license.
