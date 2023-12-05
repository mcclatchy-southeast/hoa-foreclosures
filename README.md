# HOA Foreclosures
To investigate HOA foreclosures in North Carolina, reporters for The Charlotte Observer and The News and Observer used state courts data to examine thousands of foreclosure cases, as well as the paper court files for more than 100 cases in Mecklenburg and Wake counties. Their work is the first comprehensive analysis of HOA foreclosures in North Carolina.

Reporters also interviewed six people who lost their homes to foreclosure and more than 30 others, including attorneys who represent both HOAs and homeowners. A reporter also observed a foreclosure auction at the Mecklenburg County courthouse.

Reporters obtained and analyzed a North Carolina Administrative Office of the Courts database of all civil cases from January, 2018 to June, 2023 to identify HOA-related cases. 

We discovered that 50,000 liens were filed by nearly 6,000 HOAs. In roughly 11 percent of those cases, HOAs ultimately started foreclosure proceedings.

In North Carolina, if you're 30 days behind on paying your HOA dues, the association can file a lien (CLOL filing) against your property. And if you fall 90 days behind, an HOA can move to foreclose (FORE filing) - over any debt, no matter how small. Clerks check whether the homeowner failed to pay dues, whether the HOA filed a lien, whether the HOA board authorized foreclosure and whether the association has evidence that it made required efforts to notify homeowners about its plans to foreclose. If the answer to those questions is yes, approval is virtually assured, which then results in a final account/final report (FAFR) filing, meaning the homeowner will lose their home to the highest bidder.
Key elements of the data includes the county of court, party names, party role (plaintiff or defendant), issue type (such as claim of lien and foreclosure) and filing date. In some cases, the order result and order amount is listed.

# How we did the analysis
A public records request to the N.C. Administrative Office of the Courts provided a database of all civil cases filed in North Carolina courts from January, 2018 to June 30, 2023. This includes all civil district, magistrate, superior, estate and special proceeding filings. 

Because there is no field to indicate if a plaintiff is an HOA, we used the name field to extract any case where the party name matched the following terms:
                  'HOA ', ' HOA', 'HOMEOWNERS ASSOC', 'HOMEOWNERS ASSN', 'HOME OWNERS ASSN', 'HOME OWNERS ASSOC', 'PROPERTY OWNERS ASSN', 'PROPERTY OWNERS ASSOC',
                  'COMMUNITY ASSN', 'COMMUNITY ASSOC', 'COMM ASSN', 'COMM ASSOC', 'OWNERS ASSN', 'OWNERS ASSOC', "HOMEOWNER'S ASSN", "HOMEOWNER'S ASSOC",
                  "OWNER'S ASSN", "OWNER'S ASSOC", 'ASSN OF HOMEOWNERS', 'ASSOC OF HOMEOWNERS', 'ASSN OF CO OWNERS', 'ASSOC OF CO OWNERS', 'CONDOMINIUM ASSOC',
                  'CONDOMINIUM ASSN', "OWNERS' ASSN", "OWNERS' ASSN", 'HOMEWONERS', 'COMMUNITY PROPERTY', 'TOWNHOME ASSOC', 'TOWNHOME ASSN', 'CONDOMINIUM UNIT OWNERS',
                  'HOMEOWNERS ASSOCIATION', 'HOME OWNERS ASSOCIATION', "HOMEOWNERS'S ASSOCIATION"

This produced XX HOA's. But the HOA names needed cleaning due to the different spellings of the same entity, such as: 
                  "ABC123 HOMEOWNER'S ASSN", "ABC123 HOA", "ABC 123 HOME OWNERS ASSOCIATION". 
To get the most accurate count of plaintiffs, we used a combination of [OpenRefine](https://openrefine.org/), an open-source data cleaning tool, and manual reviews and checks. This provided a reduced count of XX HOA's.

The cleaned name data was then matched with a table containing the type of issue for the case. Cases can have multipe issue types. We were primarily intestered in three issue types: claim of lien (CLOL), foreclosure (FORE) and final account/final report (FAFR). 

 



                  



