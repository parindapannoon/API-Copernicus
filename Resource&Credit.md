# API-Copernicus
All daa is provided by Climate Data Store (CDS)-- Copernicus Climate Change and ECMWF
Copernicus Climate Change Service (C3S) (2022): ERA5-Land monthly averaged data from 1950 to present. Copernicus Climate Change Service (C3S) Climate Data Store (CDS). DOI: 10.24381/cds.68d2bb30 (Accessed on 10-04-2023)
https://cds.climate.copernicus.eu/cdsapp#!/dataset/10.24381/cds.68d2bb30?tab=overview


```python

import cdsapi

c = cdsapi.Client()

c.retrieve(
    'reanalysis-era5-land-monthly-means',
    {
        'product_type': 'monthly_averaged_reanalysis',
        'variable': [
            'forecast_albedo', 'skin_temperature', 'total_precipitation',
        ],
        'year': [
            '1951', '1965', '1979',
            '1993', '2007', '2021',
        ],
        'month': '09',
        'time': '00:00',
        'format': 'grib',
    },
    'download.grib')

```


