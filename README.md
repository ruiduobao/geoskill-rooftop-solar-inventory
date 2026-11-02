# geoskill-rooftop-solar-inventory

> Inventory building rooftop solar potential: available area, slope/aspect, shading, and PV capacity/energy yield/economic viability. Outputs building-level candidate rankings for solar deployment.

See [SKILL.md](SKILL.md) for full usage, inputs and outputs.

## Quick start

```bash
# Basic analysis with synthetic demo data
python scripts/rooftop_solar_inventory.py --output-dir ./rsi-output

# With custom setback and panel type
python scripts/rooftop_solar_inventory.py \
  --setback 1.5 \
  --panel-type hjt_700w \
  --output-dir ./rsi-output

# With custom economic parameters
python scripts/rooftop_solar_inventory.py \
  --electricity-price 0.65 \
  --annual-ghi 1600 \
  --system-lifetime 30 \
  --output-dir ./rsi-output

# With building footprints file
python scripts/rooftop_solar_inventory.py \
  --buildings ./data/buildings.geojson \
  --dsm ./data/dsm.tif \
  --output-dir ./rsi-output
```

## License

MIT
