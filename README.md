# FoCS project

## Dataset Description

General info (to organize before the exam)

Zurich Transit Bus (ZTBus) dataset. 

**Data**:

- Driving missions of electric city buses in Zurich. Usually each mission covers a full day of a real operation.
- Data collected over several years on two trolley buses (due linee di filobus).
- Info about the vehicle:
    - Power demand
    - Propulsion system
    - Odometry
    - Global position
    - Ambient temperature
    - Door openings
    - Number of passanger
    - Dispatch patterns within the public transportation network
    - etc.
- All signals are synchronized in time and include an absolute timestamp in tabular form
- Dataset covers the operation of the buses on various bus routes in Zurich's public transportation network.

**File Description**

The ZTBus dataset is organized in two different types of comma-separated values (CSV) text files.

- The names of the files describing the individual driving missions are based on the vehicle identification number (either **183** or **208**) and the time period in which the data was collected.

*Example*: data collected on the bus numbered 183 between 16 Oct 2019 02:52:43 and 16 Oct 2019 07:10:12, both given in UTC, is available in the following file: B183_2019-10-16_02-52-43_2019-10-16_07-10-12.csv
    
- 1409 driving missions. Each one described in a separate CSV file.
- All files have the same structure and format:
    - First row contains the headers of the corresponding columns.
    - Remaining rows describe the set of data samples recorded at a specific moment in time.
    - This time index is represented in the first column as absolute UTC time, expressed according to `ISO 8601`.

**metaData.csv**

This file contains metadata of the driving missions in a tabular form. 

- The first row contains the headers of the corresponding columns.
- The remaining rows contain metadata of the driving missions, indexed via the corresponding file name in the first column.

**Detailed description of the variables**: Check ZT_bus_README.md


## How to run the code

Add requirements.txt for environment

## References

Widmer, F., Ritter, A., & Onder, C. H. (2023). ZTBus: A Large Dataset of Time-Resolved City Bus Driving Missions. *Scientific Data, 10*(1), Article 209. [https://doi.org/10.1038/s41597-023-02600-6](https://doi.org/10.1038/s41597-023-02600-6)
