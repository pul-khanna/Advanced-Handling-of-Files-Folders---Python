<h1> Description of Task </h1>

The folder raw.zip has raw files which were measured in a station. As the name indicates, there are 2 inverters, 1 energy meter (named MFM) and 1 meteorological
substation (named WMS). The raw data is a stream of data which gets recorded by the sensors on the field and is sent over the cloud.
We need the raw data to be transformed into the specified data format and then saved in desired folder,sub-folder structure.

*** Note: The data in the SampleGen1 files have been bucketed into 5-min intervals. Here we will ignore this operation***

<h3> Required Transformations </h3>

a. For Inverters
i. For inverters, column i32 indicates the timestamp of the row. Make this as the first column in the Gen1 file and rename the column header to ‘Timestamp’.

b. For Energy meters (MFM)
i. Same rules as above, only difference is timestamp column is m63

c. For Energy meters (MFM)
i. Same rules as above, only difference is timestamp column is w23


<h3> Folder, Sub-folder Structure (Expected Output Format) </h3>

There needs to be a Gen1 file for every raw data file. The attached raw.zip has data for each sub-station. The output format needs to be as follows:

[Station ID]
|---> [Year]
|---->[Year-Month]
|--->[Substation-ID]
|---> [Gen-1 Data.txt]

* The station ID for the given raw data is IN-023C that needs to be taken from the 'raw' data folder paths
* Year needs to be determined based on the timestamp of the file
* Year-Month needs to be determined based on the timestamp of the file
* Substation-ID depends on the sub-station name (example Inverter-1, MFM, WMS etc) and again it needs to be taken from the 'raw' data folder paths
* Gen-1 Data.txt has the same name as the raw file.txt

SampleGen1 folder is an example for our reference to see the folder, sub-folder structure with transformed/cleansed files
