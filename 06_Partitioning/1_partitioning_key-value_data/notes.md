# Partitioning of Key-Value Data

- Data must be spread evenly to respond faster to more queries
- partitioning = splitting data into smaller pieces
- Skew = uneven distribution of data
- hotspot = a partition that is accessed more than others
- Key strategies: 
  - Random partitioning -> but you don't know where to read the data
  - Key Ranging -> you know where to read the data, but it can lead to hotspots