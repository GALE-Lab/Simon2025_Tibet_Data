# Supporting Data for Cenozoic Wedge Tectonics as a Crustal Thickening Mechanism for the Min Shan, Eastern Tibetan Plateau

This Zenodo deposit contains compiled structural measurement data, geospatial mapping files, Supporting Information figure files, and supporting documentation for the manuscript:

`Cenozoic Wedge Tectonics as a Crustal Thickening Mechanism for the Min Shan, Eastern Tibetan Plateau`

Authors: Abijah Simon, Paul Kapp, and Chen Wu.

## Contents

- `2019_2018_2016_Field_measurements.xlsx`
  Multi-sheet workbook containing the same primary archive tables as the CSV files.
- `structural_plane_measurements.csv`
  Planar structural measurements used by the stereonet program, including 2019 FieldMove measurements and manually compiled 2018 measurements.
- `structural_line_measurements.csv`
  Linear structural measurements used by the stereonet program, including slickensides, fold axes, and related lineation data.
- `field_point_locations.csv`
  Unique field point locations from the KML placemarks, including 2016 field localities that do not have structural measurements in this archive.
- `Mapping_Data.kml`
  Geospatial mapping file used to visualize mapped features and measurement locations.
- `Map_Source_References.md`
  Source bibliography for geologic maps and related compilation inputs used to build the map products.
- `Figure_S1_Min_Shan_structural_measurements_map.png`
  High-resolution digital version of Supporting Information Figure S1.
- `Figure_S2_Eastern_Tibet_field_measurements_map.png`
  High-resolution digital version of Supporting Information Figure S2.
- `DATA_DICTIONARY.md`
  Field descriptions, stop-ID conventions, and notes for the workbook and CSV files.

## Data Notes

The CSV files are the preferred open-format data tables. The Excel workbook mirrors those tables for users who prefer a multi-sheet spreadsheet.

Rows are sorted in forward chronological order, from 2016 to 2018 to 2019, then by stop/locality identifier within each field season.

The first column in the measurement tables is the field stop or locality identifier. The 2019 IDs generally use `month-day-19-stop`; 2018 IDs in the KML generally use the `AS-` prefix, while the stereonet measurement CSVs may omit that prefix and leading zeroes; 2016 IDs use the `AY` prefix. See `DATA_DICTIONARY.md` for details.

Coordinate fields are stored as decimal-degree longitude and latitude values and are intended to align with the accompanying KML file. `Field Point Locations` contains one row per unique KML point placemark rather than one row per structural measurement.

The structural measurement values were compiled from the source stereonet CSV tables. Exact full-row duplicates were removed, and obvious source coordinate-column swaps in the line-measurement table were corrected.

For column definitions, row counts, stop-ID conventions, units, and data-cleaning notes, see `DATA_DICTIONARY.md`.

`Map_Source_References.md` documents the sources used to compile the map products. Sources that are explicitly cited in the manuscript or Supporting Information should also be handled through the manuscript reference workflow.

## Citation

Please cite the Zenodo DOI associated with this deposit.

## License

These data and documentation are released under the Creative Commons Attribution 4.0 International license (CC BY 4.0): https://creativecommons.org/licenses/by/4.0/

## Contact

Abijah Simon, University of California, Los Angeles: abijah@ucla.edu
