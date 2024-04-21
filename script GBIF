# Install the packages required to download the GBIF data with Julia.

using Pkg
Pkg.add("GBIF2")
Pkg.add("DataFrames")
Pkg.add("CSV")

# Use "using" to run each of the packages.

using GBIF2, DataFrames, CSV

# Initially a basic search can be performed by matching the species with "species_match". The above in order to validate the data (the common name of the species can also be used, for example, Andean condor).

sp = species_match("Vultur gryphus")

# The species is defined.

sp.species

# A search is performed by synonymy.

sp.synonym

# The search is performed by Vernacular name.

sp.vernacularName

# If required, more details of the species can be chosen.

sp_detailed = species(sp)

# If required, more details of the species with vernacular name can be chosen.

sp_detailed.vernacularName

# For this example, we are going to choose all the occurrences of Vultur gryphus with coordinates from 1900 to 2024, placing as search limit 70000 and generating a DataFrame. It should be noted that the approximate execution time was 1:30 hours, but this may vary depending on the amount of data, the species, Julia's version, etc. Date of execution: April 21, 2024.

oc = occurrence_search(sp;
           limit=70000, hasCoordinate=true, year=(1900,2024)
       ) |> DataFrame

# In total, 67626 occurrences were downloaded, which agree with all the data reported by GBIF with coordinates. Subsequently, we place the address where we are going to save the information, for this case in downloads and the name of the file in CSV.

archivo_csv = "C:/Users/caden/Downloads/ocurrencias_Vultur_gryphus.csv"

# We write the CSV file with all the occurrences of the chosen information.

CSV.write(archivo_csv, oc)

# Finally, we verify the address of the saved file.

println("Occurrences saved in: $archivo_csv")
