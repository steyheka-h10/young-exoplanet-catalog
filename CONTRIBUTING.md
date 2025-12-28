# Contribution Guidelines and Entry Template

This document describes the required format for adding new entries to the Young Exoplanet Catalog.

## Entry Format

All new entries must be added as a new `.yaml` file in the `data/` directory. The filename should be the planet name in lowercase with hyphens, e.g., `beta-pictoris-b.yaml`.

## YAML Template

Each YAML file must contain the following fields:

```yaml
planet_name: "Example Planet b"
host_star: "Example Star"
system_age_myr: 50
detection_method: "Direct Imaging"
orbital_radius_au: 10.0
mass_jupiter: 5.0
reference_doi: "10.1086/123456"
notes: ""
```

### Field Descriptions

- **planet_name**: Common designation of the exoplanet (string).
- **host_star**: Name of the host star (string).
- **system_age_myr**: Age of the planetary system in millions of years (integer or float). Must be < 500 Myr.
- **detection_method**: Primary discovery method (string). Examples: "Direct Imaging", "Radial Velocity", "Transit", "Microlensing", "Astrometry".
- **orbital_radius_au**: Semimajor axis in astronomical units (float).
- **mass_jupiter**: Mass in Jupiter masses (float). Use `null` or provide upper/lower limits as strings if uncertain.
- **reference_doi**: Digital Object Identifier of the primary reference paper (string). Should be a valid DOI.
- **notes**: Optional free‑text field for additional remarks (string). Leave empty if not needed.

## Quality Control

- Please verify the data from reliable sources (peer‑reviewed papers, NASA Exoplanet Archive, etc.).
- Keep the YAML syntax valid (consistent indentation, proper quoting).
- Before opening a pull request, ensure your entry follows this template exactly.

## Pull Request Process

1. Fork the repository.
2. Create a new branch for your entry.
3. Add the YAML file to `data/`.
4. Open a pull request with a descriptive title (e.g., "Add data for [Planet Name]").
5. In the PR description, reference these guidelines and confirm that the entry adheres to them.

Thank you for contributing to the catalog!