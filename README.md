dat - DICOM anonymization tool
==========
A python script that uses the DicomSummarize command line tool installed from
DicomBrowser. You can get the DicomBrowser here:

https://wiki.xnat.org/xnat-tools/dicombrowser

To anonymize a DICOM named `deanon.dcm` to `anon.dcm` using the tags specified
in `remap-config-file.xml`:

```bash
dat anonymize deanon.dcm anon.dcm --config-xml remap-config-file.xml \
 --remap-csv remap.csv
```

This creates a file called `remap.csv` that contains the stripped out fields.
This file is used to put the data back in later:

```bash
dat deanonymize anon.dcm deanon.dcm --config-xml remap-config-file.xml \
 --remap-csv remap.csv
```

