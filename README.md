# HOA Foreclosures
To investigate HOA foreclosures in North Carolina, The Charlotte Observer and The News & Observer conducted a first-of-its-kind analysis of HOA foreclosures in North Carolina.

News & Observer data reporter David Raynor analyzed a North Carolina Administrative Office of the Courts database of all civil cases from January, 2018 to June, 2023 to identify HOA-related foreclosure filings.

Charlotte Observer investigative reporter Ames Alexander then reviewed court files in more than 100 foreclosure cases in Mecklenburg and Wake counties to gather more detailed information on each case.

Alexander interviewed six people who lost their homes to HOA foreclosures and more than 30 others, including attorneys who represent both HOAs and homeowners. And he observed a foreclosure auction at the Mecklenburg County courthouse.

As part of the data analysis, Raynor discovered that 50,000 liens were filed by nearly 6,000 North Carolina HOAs between 2018 and mid 2023. In roughly 11% of those cases, HOAs started foreclosure proceedings. More details on the analysis can be found here.

In North Carolina, if you're 30 days behind on paying your HOA dues, the association can file a lien (CLOL filing) against your property. And if you fall 90 days behind, an HOA can move to foreclose (FORE filing) - over any debt, no matter how small. Clerks check whether the homeowner failed to pay dues, whether the HOA filed a lien, whether the HOA board authorized foreclosure and whether the association has evidence that it made required efforts to notify homeowners about its plans to foreclose. If the answer to those questions is yes, approval is virtually assured, which then results in a final account/final report (FAFR) filing, meaning the homeowner will lose their home to the highest bidder.

# How we did the analysis
A public records request to the N.C. Administrative Office of the Courts provided a database of all civil cases filed in North Carolina courts from January, 2018 to June 30, 2023. This includes all civil district, magistrate, superior, estate and special proceeding filings. 

Key elements of the data include the county of court, party names, party role (plaintiff or defendant), issue type (such as claim of lien and foreclosure) and filing date. In some cases, the order result and order amount is listed.

There is no clear indicator in the data that a party name is an HOA. Therefore, we used the name field to extract cases where the party name matched any of the following terms: <br>
                  'HOA ', ' HOA', 'HOMEOWNERS ASSOC', 'HOMEOWNERS ASSN', 'HOME OWNERS ASSN', 'HOME OWNERS ASSOC', 'PROPERTY OWNERS ASSN', 'PROPERTY OWNERS ASSOC',
                  'COMMUNITY ASSN', 'COMMUNITY ASSOC', 'COMM ASSN', 'COMM ASSOC', 'OWNERS ASSN', 'OWNERS ASSOC', "HOMEOWNER'S ASSN", "HOMEOWNER'S ASSOC",
                  "OWNER'S ASSN", "OWNER'S ASSOC", 'ASSN OF HOMEOWNERS', 'ASSOC OF HOMEOWNERS', 'ASSN OF CO OWNERS', 'ASSOC OF CO OWNERS', 'CONDOMINIUM ASSOC',
                  'CONDOMINIUM ASSN', "OWNERS' ASSN", "OWNERS' ASSN", 'HOMEWONERS', 'COMMUNITY PROPERTY', 'TOWNHOME ASSOC', 'TOWNHOME ASSN', 'CONDOMINIUM UNIT OWNERS',
                  'HOMEOWNERS ASSOCIATION', 'HOME OWNERS ASSOCIATION', "HOMEOWNERS'S ASSOCIATION"

This produced approximately 10,400 HOA's filing more than 50,000 cases, mostly for claim of liens and foreclosures. But the HOA names needed cleaning due to the different spellings of the same entity, such as: 
                  "ABC123 HOMEOWNER'S ASSN", "ABC123 HOA", "ABC 123 HOME OWNERS ASSOCIATION". 

To get the most accurate count of HOA plaintiffs, we used a combination of [OpenRefine](https://openrefine.org/), an open-source data cleaning tool, and manual reviews and checks. This provided a more accurate count of approximately 5,700 HOA's.

The cleaned name data was then matched with a table containing the type of issue for the case based on the case number and county code. Cases can have multipe issue types. We were primarily intestered in three issue types: claim of lien (CLOL), foreclosure (FORE) and final account/final report (FAFR). In other words, how many HOA's began the process of foreclosure with a lien filing, how many moved to the next stage of filing the foreclosure and how many moved to force the owner out and sale the home.

A case could have been included in all three issue type filings, but was only counted once in each category. 

![HS0GO-hoa-foreclosure-filings](https://github.com/mcclatchy-southeast/hoa-foreclosures/assets/65453792/c8fa9d58-41eb-438d-a934-5779473fc703)

 
 



                  



