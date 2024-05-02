# A-Replication-of-Currency-Boards-in-Retrospect-and-Prospect

<ins>Main Data Spreadsheet</ins>

The two main spreadsheets in this paper is IMF's World Economic Outlook (WEO) (April 2024) and International Financial Statistics (IFS) (2023) database. Both spreadsheet are located in the folder "MainSpreadsheet". Other spreadsheet for individual series and their folders are listed below:

| Variable                           | Folder/Filename                                               |
| -----------------------------------| --------------------------------------------------------------|
| Wolf et al.'s original spreadsheet | CBRDATA/LDTEST1.XLS                                           |
| World GDP growth                   | Trade/imf-dm-export-20240420.xlsx                             |
| Income Level                       | List_of_countries.xlsx                                        |
| Exchange Rate Regime               | Regimes/REGIMETS_2023.xlsx                                    |
| Sovereign Debt                     | SovereignDebt/SOVD-data-from-Schuler.xlsx                     |
| Central Bank Turnover              | Cbturn/CBGOV-data-from-Dreher.xlsx                            |
| Currency Control                   | CURCON-KAPCON/CURCON-data-from-AREAR.xlsx                     |
| Capital Control                    | CURCON-KAPCON/KAPCON-data-from-Chinn-Ito.xlsx                 |
| Trade Data                         | Trade/Trade-data-from-IMF-DOTS-database 2023Q4.xlsx           |
| Banking Crisis                     | Crisis/BNKSTRT-data-from-Metrick-Schmelzing-plus-Schuler.xlsx |

Other files not listed here are compiled by Wolf et al.

<ins>Consolidating spreadsheets</ins>

To consolidate all spreadsheets into 1 main spreadsheet, run the following notebooks in the folder MainSpreadsheet. Duplicated series are taken from WEO database first. Then, we fill any missing datapoints with data from IFS database and Wolf et al.'s orinal spreadsheet in that order. Due to rebasing issues, some nominal series such as price level and nominal GDP may have some discrepancies, but the growth rate series are reliable.

1. Wolf-base.ipynb
2. WEO-base.ipynb
3. IFS-base.ipynb
4. Combine-excel.ipynb

The consolidated spreadsheet is located at "MainSpreadsheet/CombinedData.xlsx" and is ready for statistical tests. When new data are available, you can rerun notebook 2-4 to create updated spreadsheets.

<ins>Statistical tests</ins>

All tests are done in "Testing.ipynb".

<ins>A Note on the Data</ins>

Wolf et al. (2008) assembled macroeconomic data on more than 160 countries, from 1970 to 2002, mainly from statistics reported to the International Monetary Fund (IMF) by its member countries. Their data included statistics for the currency boards or quasi currency boards of Argentina, Bosnia and Herzegovina, Bulgaria, Djibouti, Estonia, Hong Kong, and Lithuania. Their data also included statistics for the members of the Eastern Caribbean Central Bank (ECCB) that were members of the IMF (Antigua and Barbuda, Dominica, Grenada, St. Lucia, St. Kitts and Nevis, and St. Vincent and the Grenadines). The IMF classifies the ECCB as a currency board even though some other observers do not (Carpenter 2016).

This paper builds on Wolf et al. by updating the data to 2023. They kindly provided their data as the building block of this paper and one of them, Dr. Atish R. Ghosh, patiently answered questions about their data and procedures on behalf of his coauthors. The bibliography lists the sources of data in the accompanying spreadsheets. The major sources for updating Wolf et al.’s data are databases for three IMF publications: the World Economic Outlook, International Financial Statistics, and the Annual Report on Exchange Rate Arrangements and Exchange Restrictions.

 Further data and analysis have resulted in a few improvements over Wolf et al.:

•	Data are available for nearly 40 more countries, including two additional currency board systems, Brunei and Macau. (Several small jurisdictions with currency boards remain outside the datasets both of Wolf et al. and this paper: Bermuda, Cayman Islands, Falkland Islands, Gibraltar, Guernsey, Isle of Man, Jersey, St. Helena, and the ECCB members Anguilla and Montserrat.)

•	Some historical data not available to Wolf et al. for the countries and years they covered are available now.

•	To add more detail and, one hopes, clarity to the types of monetary regimes, this paper distinguishes dollarized regimes from both currency boards and pegged regimes.

•	Wolf et al. do not distinguish monobanks, which monopolize both central banking and commercial banking, from typical central banks, which do not monopolize commercial banking. This paper removes monobanks from data on central banks.

Old data from Wolf et al. were generally compatible with updated data. A partial exception was that there have been substantial revisions to some data on GDP levels. Changes to estimates of GDP growth rates, which are what matter in the tests, are however smaller. The order of preference for using data is (1) World Economic Outlook database, (2) the current International Financial Statistics database, (3) Wolf et al. data from older IMF data. For some series there are also data from other sources. This paper omits tests of some variables in Wolf et al., notably those involving years of schooling and banking crises, for which comprehensive and comparable updated data did not seem to be readily available.
