# Min Shan Tectonics Supporting Data

This repository contains compiled structural measurement data, geospatial mapping files, and supporting documentation for the manuscript:

`Cenozoic Wedge Tectonics as a Crustal Thickening Mechanism for the Min Shan, Eastern Tibetan Plateau`

Authors: Abijah Simon, Paul Kapp, and Chen Wu.

## Contents

- `2019_2018_2016_Field_measurements.xlsx`
  Multi-sheet workbook containing the same primary archive tables as the CSV files.
- `csv/structural_plane_measurements.csv`
  Planar structural measurements used by the stereonet program, including 2019 FieldMove measurements and manually compiled 2018 measurements.
- `csv/structural_line_measurements.csv`
  Linear structural measurements used by the stereonet program, including slickensides, fold axes, and related lineation data.
- `csv/field_point_locations.csv`
  Field point and measurement locations for cross-reference with the KML placemarks, including 2016 field localities that do not have structural measurements in this archive.
- `Mapping_Data.kml`
  Geospatial mapping file used to visualize mapped features and measurement locations.
- `Map_Source_References.docx`
  Source bibliography for geologic maps and related compilation inputs used to build the map products.
- `Map_Source_References.md`
  Plain-text Markdown export of `Map_Source_References.docx`.
- `DATA_DICTIONARY.md`
  Field descriptions, stop-ID conventions, and notes for the workbook and CSV files.
- `CITATION.cff`
  Citation metadata for GitHub and citation-management tools.
- `.zenodo.json`
  Zenodo metadata for the archived release.

## Data Notes

The CSV files are the preferred open-format data tables. The Excel workbook mirrors those tables for users who prefer a multi-sheet spreadsheet.

Rows are sorted in forward chronological order, from 2016 to 2018 to 2019, then by stop/locality identifier within each field season.

The first column in the measurement tables is the field stop or locality identifier. The 2019 IDs generally use `month-day-19-stop`; 2018 IDs in the KML generally use the `AS-` prefix, while the stereonet measurement CSVs may omit that prefix and leading zeroes; 2016 IDs use the `AY` prefix. See `DATA_DICTIONARY.md` for details.

Coordinate fields are stored as decimal-degree longitude and latitude values and are intended to align with the accompanying KML file.

The structural measurement values were compiled from the stereonet input CSV files used by the companion analysis code. Exact full-row duplicates were removed, and obvious source coordinate-column swaps in the line-measurement table were corrected.

`Map_Source_References.md` documents the sources used to compile the map products. It is included as repository documentation for the archived data package; sources that are explicitly cited in the manuscript or supporting information should also be handled through the manuscript reference workflow.

## Citation

For the preserved archival version, cite the Zenodo DOI associated with the release. For the live development repository, cite:

Simon, A., Kapp, P., & Wu, C. (2025). Min Shan Tectonics Supporting Data. GitHub repository. https://github.com/GALE-Lab/Simon2025_Tibet_Data

## License

These data and documentation are released under the Creative Commons Attribution 4.0 International license. See `LICENSE`.

## Contact

Abijah Simon, University of California, Los Angeles: abijah@ucla.edu
