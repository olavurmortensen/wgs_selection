
The AEBS repository is used to read data from exported data from Ættarbandsskráin, and to reconstruct the genealogy of the individuals in the Fargen cohort. The raw and "cleaned" GEDCOM file can be found in data/ged. The full genealogy and the FarGen genealogy can be found in data/trees.

First add the AEBS scripts to path:

cd aebs
source setup.sh
cd ..

Clean up the raw GEDCOM file:

ged_cleanup.sh data/ged/aebs_export_2020-06-18/aebs_export_2020-06-18.ged data/ged/cleaned.ged

Extract certain fields from the cleaned GEDCOM file and write it to a CSV:

ged2csv data/ged/cleaned.ged data/trees/aebs.csv

Before we can reconstruct the FarGen genealogy, we must obtain the IDs of the individuals. To do that, we need the P-number of the FarGen individuals, and we shall match them with the P-numbers in the GEDCOM file.

Below we extract the REFN and RIN fields from the cleaned GEDCOM file. The REFN field contains the P-number.

ged2csv.py data/ged/cleaned.ged data/ids/aebs_ids.csv

We obtain information about the FarGen individual from the Progeny database. The "fargen_ids.csv" file from Progeny contains the FarGen individual IDs FN and their P-numbers. Below we match FarGen individuals with individuals in the genealogy registry, and obtain their RIN and FN IDs in a CSV, and only their RIN in a text file.

python match_ids.py data/ids/fargen_ids.csv data/ids/aebs_ids.csv fargen_rin_samplename.csv fargen_rin.txt

Now we can reconstruct the FarGen genealogy:

python lineages.py --csv data/trees/aebs.csv --ind data/ids/fargen_rin.txt --out data/trees/fargen.csv

The "data/placenames/placename_regions.csv" file contains the names of the 200 most common birth places in the genealogy registry. The placenames are cleaned up with a function in the "data/placenames/clean_placename.py" script, to reduce the number of unique placenames.

Get a list of the 200 most common birth places:

python data/placenames/birth_locations_cleanup.py data/trees/aebs.csv data/placenames/placename_regions.csv

Then I have manually edited the data/placenames/placename_regions.csv file, adding the "region" column, so that each birth place is associated with a geographical region (1-6).

Then make a list of RIN and region, so that each individual is attributed a regional birth place identifier:

python data/placenames/placename2region.py data/placenames/placename_regions.csv data/trees/aebs.csv data/placenames/rin_region.csv





