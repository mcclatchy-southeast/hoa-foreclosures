# HOA Foreclosures
To investigate HOA foreclosures in North Carolina, The Charlotte Observer and The News & Observer conducted a first-of-its-kind analysis of HOA foreclosures in North Carolina.

News & Observer data reporter David Raynor analyzed a North Carolina Administrative Office of the Courts database of all civil cases from January, 2018 to June, 2023 to identify HOA-related foreclosure filings.

Charlotte Observer investigative reporter Ames Alexander then reviewed court files in more than 100 foreclosure cases in Mecklenburg and Wake counties to gather more detailed information on each case.

Alexander interviewed six people who lost their homes to HOA foreclosures and more than 30 others, including attorneys who represent both HOAs and homeowners. And he observed a foreclosure auction at the Mecklenburg County courthouse.

As part of the data analysis, Raynor discovered that 50,000 liens were filed by nearly 6,000 North Carolina HOAs between 2018 and mid 2023. In roughly 11% of those cases, HOAs started foreclosure proceedings. More details on the analysis can be found here.

In North Carolina, if you're 30 days behind on paying your HOA dues, the association can file a lien (CLOL filing) against your property. And if you fall 90 days behind, an HOA can move to foreclose (FORE filing) - over any debt, no matter how small. Clerks check whether the homeowner failed to pay dues, whether the HOA filed a lien, whether the HOA board authorized foreclosure and whether the association has evidence that it made required efforts to notify homeowners about its plans to foreclose. If the answer to those questions is yes, approval is virtually assured, which then results in a final account/final report (FAFR) filing, meaning the homeowner will lose their home to the highest bidder.

# How we did the analysis
A public records request to the N.C. Administrative Office of the Courts provided a database of all civil cases filed in North Carolina courts from January, 2018 to June 30, 2023. This includes all civil district, magistrate, superior, estate and special proceeding filings. 

Key elements of the data include the county of court, party names, party role (plaintiff or defendant), issue type (such as claim of lien and foreclosure) and filing date. In some cases, the order result and order amount was listed.

There is no clear indicator in the data that a party name is an HOA. Therefore, we used the name field to extract cases where the party name matched any of the following terms: <br>
                  'HOA ', ' HOA', 'HOMEOWNERS ASSOC', 'HOMEOWNERS ASSN', 'HOME OWNERS ASSN', 'HOME OWNERS ASSOC', 'PROPERTY OWNERS ASSN', 'PROPERTY OWNERS ASSOC',
                  'COMMUNITY ASSN', 'COMMUNITY ASSOC', 'COMM ASSN', 'COMM ASSOC', 'OWNERS ASSN', 'OWNERS ASSOC', "HOMEOWNER'S ASSN", "HOMEOWNER'S ASSOC",
                  "OWNER'S ASSN", "OWNER'S ASSOC", 'ASSN OF HOMEOWNERS', 'ASSOC OF HOMEOWNERS', 'ASSN OF CO OWNERS', 'ASSOC OF CO OWNERS', 'CONDOMINIUM ASSOC',
                  'CONDOMINIUM ASSN', "OWNERS' ASSN", "OWNERS' ASSN", 'HOMEWONERS', 'COMMUNITY PROPERTY', 'TOWNHOME ASSOC', 'TOWNHOME ASSN', 'CONDOMINIUM UNIT OWNERS',
                  'HOMEOWNERS ASSOCIATION', 'HOME OWNERS ASSOCIATION', "HOMEOWNERS'S ASSOCIATION"

This produced approximately 10,400 HOA's filing more than 50,000 cases, mostly for claim of liens and foreclosures. But the HOA names needed cleaning due to the different spellings of the same entity, such as: 
                  "ABC123 HOMEOWNER'S ASSN", "ABC123 HOA", "ABC 123 HOME OWNERS ASSOCIATION". 

To get the most accurate count of HOA plaintiffs, we used a combination of [OpenRefine](https://openrefine.org/), an open-source data cleaning tool, and manual reviews and checks. This provided a more accurate count of approximately 5,700 HOA's.

The cleaned name data was then matched with a table containing the type of issue for the case based on the case number and county code. Cases can have multiple issue types. We were primarily interested in three issue types: claim of lien (CLOL), foreclosure (FORE) and final account/final report (FAFR). In other words, how many HOA's began the process of foreclosure with a lien filing, how many moved to the next stage of filing the foreclosure and how many moved to force the owner out and sale the home.

To get the most accurate count of cases, we counted each case only once in each issue type filing because a case can include all three issue type filings (or other filing types). Cases can also be filed for multiple homeowners for a single property or cases can be filed for shared ownership in a timeshare. 

We found approximately 51,000 claim of liens filed by HOAs; approximately 5,500 foreclosure filings; and approximately 600 final account/final report filings, indicating the home was sold or the timeshare owner lost access to the property.

For the analysis, we used [R](https://www.r-project.org/about.html), an open-source statistical software program; Excel; and Google Sheets. 

# Data
The case file data, including county, case number, plaintiff name and issue type, is available for [download here](https://github.com/mcclatchy-southeast/hoa-foreclosures/tree/main/data).
Issue types included: CLOL - claim of lien; FORE - foreclosure; FAFR - final account/final report. This file contains all HOA related cases filed from 2018 to 2022 where a claim of lien, foreclosure or final account/final report issue type was filed. 

If you have questions about the data or the stories in general, please contact David Raynor at draynor@newsobserver.com or Ames Alexander at aalexander@charlotteobserver.com

# Stories
[Hopes Foreclosed](https://www.newsobserver.com/news/state/north-carolina/article279816769.html) 

[Deceit, rigged bids and extortion: How HOA foreclosures can open the door to predators](https://www.newsobserver.com/news/state/north-carolina/article281805243.html) 

[‘Once. Twice. Sold for $4,400.’ How HOA foreclosure auctions cost owners their homes](https://www.newsobserver.com/news/state/north-carolina/article282167538.html) 

[Can an HOA sell your home? What NC law says, and how to challenge foreclosures](https://www.newsobserver.com/news/state/north-carolina/article282815028.html) 




