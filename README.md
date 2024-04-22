# Download of occurrences of the GBIF with Julia
Here I perform a simple exercise with the Vultur gryphus species for the option and download of GBIF occurrence data with the use of Julia software version 1.10.2.

1. The packages are implemented:
* GBIF2: To download the data from the Global Biodiversity Information Facility (GBIF) database, by using its application programming interface (API).
* Dataframe: For the manipulation and modulation of data.
* CSV: For the download and easy handling of the data on my computer.
2. The Vultur gryphus species to be worked with is searched and defined.
3. A total of 67,626 occurrences were downloaded for the species Vultur gryphus, demonstrating once again the advantages and benefits of Julia for the management of large databases.
4. The downloaded CSV file is verified with all the information.

For more details check the script, as I implement tags (#) in each line of the code to give more clarity.

References

* https://github.com/rafaqz/GBIF2.jl?tab=readme-ov-file
* https://github.com/JuliaData/CSV.jl
* https://github.com/JuliaData/DataFrames.jl
* Bezanson, J., Edelman, A., Karpinski, S., & Shah, V. B. (2017). Julia: A fresh approach to numerical computing. SIAM review, 59(1), 65-98.
