### Procedure
0. Data cleaning
 * duration:To convert monthly information like "3 months" into an integer, assuming one month is equivalent to 40 hours, you simply multiply the number of months by 40. For example, for 3 months: 3 months×40 hours=120 hours
1. Use the Import data wizard to import each of the two datasets: "courses.csv" and the Library folder containing research papers (For "courses.csv" make sure you select the cognitive services you created, not the free tier. For the research papers, you can use the free tier since we have limited the dataset to only 19 papers.)
2. Select the appropriate enrichments to be added during import (refer back to your design requirements here)
3. Customize your target index based on your design requirements to select the appropriate fields for retrieval, filtering, sorting, faceting, and searching.
4. Using the Search Explorer interface, write query strings demonstrating at minimum the following from each index:
    * Search with correct fields returned from each dataset
        * search=MS*
        * search=RESEARCH*
    * Filtering, faceting, and sorting from each dataset (as appropriate)
