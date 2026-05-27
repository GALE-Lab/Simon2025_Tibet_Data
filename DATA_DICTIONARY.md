# Data Dictionary

This file documents the tabular data in `2019_2018_2016_Field_measurements.xlsx` and the CSV files in `csv/`.

## Workbook And CSV Files

The Excel workbook mirrors the primary archive CSV tables.

Rows are sorted in forward chronological order by field date and stop/locality identifier. In `Field Point Locations`, the explicit `field_season` column is used to keep 2016, 2018, and 2019 points grouped correctly.

| Workbook sheet | CSV export | Rows including header | Description |
| --- | --- | ---: | --- |
| `Plane Measurements` | `csv/structural_plane_measurements.csv` | 4427 | Planar structural measurements used by the stereonet program, including 2019 FieldMove measurements and manually compiled 2018 measurements. |
| `Line Measurements` | `csv/structural_line_measurements.csv` | 2048 | Linear structural measurements used by the stereonet program, including slickensides, fold axes, and related lineation data. |
| `Field Point Locations` | `csv/field_point_locations.csv` | 4370 | Field point and measurement locations exported from the earlier workbook tabs for cross-reference with the KML placemarks, including 2016 field localities without structural measurements. |

## Stop Identifier Conventions

The first column in the measurement tables is the field stop or locality identifier.

- 2019 stop IDs generally use `month-day-19-stop`, for example `5-21-19-12`, and were collected with FieldMove Clino.
- 2018 stop IDs in the KML and point-location table generally use the `AS-` prefix, for example `AS-06-9-18-10A`, and correspond to Brunton/manual field measurements by Abijah Simon.
- 2018 stop IDs in the stereonet plane and line measurement CSVs may omit the `AS-` prefix and leading zeroes, for example `6-9-18-10A`.
- 2016 stop IDs use the `AY` prefix, for example `AY09-16-16-2`, for the An Yin-led field excursion.

The accompanying KML file provides geolocated stop locations. Stop IDs in the measurement tables should be cross-referenced with KML placemarks by identifier where available and by latitude/longitude coordinates where identifier formatting differs.

The strike, dip, plunge, and trend values in the measurement sheets were compiled from the stereonet input CSV files used by the companion analysis code. `Field Point Locations` is primarily a location cross-reference table and does not duplicate every structural measurement in the plane and line measurement tables.

## Coordinate Fields

Coordinate values are decimal degrees and are intended to align with the accompanying KML file. Longitude and latitude are stored as separate columns in all CSV tables.

## `structural_plane_measurements.csv`

| Field | Description | Units / format |
| --- | --- | --- |
| `Locality` | Field stop or locality identifier. | Text |
| `Latitude` | Latitude of the measurement location. | Decimal degrees |
| `Longitude` | Longitude of the measurement location. | Decimal degrees |
| `Unit` | Mapped geologic or stratigraphic unit associated with the measurement, where recorded. | Text |
| `Plane Type` | Type of planar feature measured, such as foliation, bedding, or fault. | Text |
| `strike` | Strike azimuth of the measured planar feature. | Degrees |
| `dip` | Dip angle of the measured planar feature. | Degrees |
| `altitude (m)` | Elevation of the measurement location, where recorded. | Meters |

## `structural_line_measurements.csv`

| Field | Description | Units / format |
| --- | --- | --- |
| `Locality` | Field stop or locality identifier. | Text |
| `Longitude` | Longitude of the measurement location. | Decimal degrees |
| `Latitude` | Latitude of the measurement location. | Decimal degrees |
| `Unit or Fault` | Mapped unit, fault, or feature category associated with the line measurement. | Text |
| `Line Type` | Type of linear feature measured, such as slickenside or fold axis. | Text |
| `Plunge` | Plunge of the measured lineation. | Degrees |
| `Trend` | Trend azimuth of the measured lineation. | Degrees |
| `Altitude` | Elevation of the measurement location, where recorded. | Meters |
| `notes` | Notes on kinematics or measurement context. | Text |

## `field_point_locations.csv`

| Field | Description | Units / format |
| --- | --- | --- |
| `source_sheet` | Earlier workbook sheet from which the point-location row was exported. | Text |
| `field_season` | Field season year. | Year |
| `kml_stop_id` | Stop identifier as used in the point-location table and KML placemarks. | Text |
| `longitude` | Longitude of the field point. | Decimal degrees |
| `latitude` | Latitude of the field point. | Decimal degrees |
| `unit` | Mapped geologic or stratigraphic unit where present in the earlier workbook. | Text |
| `plane_type` | Plane type where present in the earlier workbook. | Text |
| `strike` | Strike where present in the earlier workbook. | Degrees |
| `dip` | Dip where present in the earlier workbook. | Degrees |
| `altitude_m` | Elevation where present in the earlier workbook. | Meters |
| `description` | Optional point-location description. | Text |

## Notes For Reuse

- Empty cells are preserved as empty CSV fields.
- The CSV tables are the preferred open-format data files for reuse.
- The Excel workbook is included for users who prefer a multi-sheet workbook.
- Exact full-row duplicates present in the stereonet input files were removed from the archive tables.
- The `5-16-18-1B` measurement locality and `AS-05-16-18-1B` point-location identifier were standardized to match the KML placemark.
- Line-measurement rows with impossible latitude values inherited from swapped source columns were corrected so longitude and latitude are in the documented columns.
- The map-source bibliography is provided in both Word (`Map_Source_References.docx`) and Markdown (`Map_Source_References.md`) formats.
