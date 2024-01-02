# STORM-preprocessing
These are the scripts to conduct the data-preprocessing for the STORM model. Input data is taken from IBTrACS, see https://www.ncdc.noaa.gov/ibtracs/. 

以下、津田

# 実行方法

## 必要なデータ
1. IBTrACS


https://www.ncei.noaa.gov/data/international-best-track-archive-for-climate-stewardship-ibtracs/v04r00/access/netcdf/


上記サイトより、「IBTrACS.since1980.v04r00.nc」をダウンロード

2. ERA5

get_era5_MSLP.ipynb, get_era5_SST.ipynbを使用して、データをダウンロード

※ CDS API keyの 取得が必要

## 実行方法
```python
python master_preprocessing.py
```

以上、津田

**IMPORTANT: Please be aware that these scripts are not maintained and NO support is provided!!**

Please run the scripts as follows:

1. preprocessing.py (this is a module)
2. coefficients.py  (this is a module)
3. environmental.py (this is a module)
4. Make_land_ocean_mask.py <-- in Python 2.7 (uses Basemap), this file stores a .txt file that can be loaded in Python 3.x. These files are now added to the repository, see the Land_ocean_mask_{basin}.txt files
5. genesis_matrix.py  (this is a module)
6. master_preprocessing.py  (this is the master script using the other modules)
