## Data from the Indian Meteorological Department (IMD)

The IMD develops several datasets with wide applicability across research and industry, but the dissemination of these datasets is often inadequate. This repository is an attempt to collate some of these datasets and present them in a more user-friendly format.


### Description
|  Dataset | Spatial resolution | Temporal resolution |   Period  | Notes                                |
|:--------:|:------------------:|:-------------------:|:---------:|:--------------------------------------:|
| `tmax`     |        1° x 1°       |        1 day        | 1951-2020 |                                  -    |
| `tmin`     |        1° x 1°       |        1 day        | 1951-2020 |                                  -    |
| `rainfall` |     0.25° x 0.25°    |        1 day        | 1901-2021 | 2005 data missing; filled with `nan` |


### Organization
The data are stored in the `data` directory, with separate sub-directories for each dataset. The data are available in multiple formats, including netcdf, which is what most users will need. The netcdfs are available at the general path `data/<dataset>/netcdf/<dataset>_<YYYY>.nc`. For example, the netcdf file containing `tmax` data from 2013 is available at `data/tmax/netcdf/tmax_2013.nc`. 

Besides the data there is also a sample Jupyter notebook in the `notebooks` directory showing how the data can be open, analysed, and visualized using Python. 

### Usage
The data can be accessed either by cloning the repository via `git clone https://github.com/vidurmithal/imd_data.git` or by downloading the repository locally as a zip folder. 

To run the notebook, certain Python packages are required, which are listed in the [requirements.txt](requirements.txt) file. These can be installed by running `pip install -r requirements.txt`.  

### References
#### Temperature dataset
Srivastava, A. K., M. Rajeevan, and S. R. Kshirsagar. "Development of a high resolution daily gridded temperature data set (1969–2005) for the Indian region." _Atmospheric Science Letters_ 10, no. 4 (2009): 249-254.

#### Rainfall dataset
Pai, D. S., M. Rajeevan, O. P. Sreejith, B. Mukhopadhyay, and N. S. Satbha. "Development of a new high spatial resolution (0.25× 0.25) long period (1901-2010) daily gridded rainfall data set over India and its comparison with existing data sets over the region." _Mausam_ 65, no. 1 (2014): 1-18.
