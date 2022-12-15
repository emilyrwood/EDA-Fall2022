# EDA-Fall2022
ENV 872 - Environmental Data Analytics, Fall 2022

# <Wood_ENV872_Project>

## Summary

Poaching remains a considerable threat to biodiversity across the planet. However, it often is overshadowed by other environmental issues in the policy realm. This is especially true for species that aren't charismatic mega-fauna. I'm undertaking this research project to better understand the trends in poaching over time and understand the regions where the most risk is occuring. This could help target poaching hotspots and help policy makers make more informed decisions when it comes to mitigating poaching risk for sesitive species. 

Main Questions:

Is there any correlation between class, term, appendix number and poaching amount?

Sub Questions:

What is the distribetion of amounts found exported and imported for all species included in the database?

Are there differences between Appendix Levels for the amount exported vs. imported?

What are the most commonly poached classes between Appendix Levels?

What are the top 3 Classes for species poached in Appendix I?

What are the dominant good types (terms) for the top 3 classes poached in Appendix I?

Which Counties are the biggest Importer and Exporters of CITES species?


\newpage

## Investigators

Emily Wood
508-361-6615
erw46@duke.edu

## Keywords

Poaching
Trafficking 
Trade
International 
Export
Import

## Database Information

The Convention on International Trade in Endangered Species of Wild Fauna and Flora (CITES) is an international agreement between governments. This group studies poaching trends and advises the UN on necessary action to mitigate this risk. This CITES dataset contains records on every international import or export conducted with species from the CITES monitoring list in 2016 and 2017. It contains columns identifying the species, the import and export countries, and the amount and characteristics of the goods being traded (which range from live animals to skins and cadavers). 


## Folder structure, file formats, and naming conventions 

Code - Code contains .R files for analysis,exploration,processing, and wrangling

Data_Raw - Dataframe as is when downloaded from CITES. This is a .CSV file.

Data_Processed - Dataframe after processing and wrangling. This is a .CSV file.

Output - Output materials. THis is a .pdf and a .html file. 

READ_ME - Basic information on the project. (this document. )

Everything is names according to the code it contains. 

## Metadata

CITESPoaching2016

"Year" - Either 2016 or 2017, categorical
"Appendix"  - I, II, II (From most to least impacted by poaching), categorical
"Taxon"  - The species' taxonomic taxon, categorical                  
"Class"  - The species' taxonomic class, categorical                   
"Order"   - Order of the species, categorical                
"Family"   - Family of the species, categorical
"Genus"  - Genus of the species, categorical                    
"Importer"  - Country that was importing the occurrence, categorical                 
"Exporter"  - Country that was exporting the occurrence, categorical               
"Origin"  - Country of origin for the occurrence, categorical                  
"Importer_reported_quantity" - Count, numeric 
"Exporter_reported_quantity" - Count, numeric 
"Term"  - Types of good, categorical                  
"Unit"  - Measurement (count,g, kg), categorical                    
"Purpose"  - Intended use, categorical               
"Source" -  Describes how the animal or plant species was brought onto the market: bred, captured wild, zoo specimen, etcetera, categorical                  
"Reported_quantity" - combination of import and export quantity, numeric     


## Scripts and code

library('formatR') - reformat r code to improve readability 
library(tidyverse) - data science packages 
library(agricolae) - helps with plot designs 
library(ggplot2) - plot packaging 
library(rworldmap) - Mapping for countries 

## Quality assurance/quality control

Class appears to leave out the two plant classes. They are contianed in the NAs. Unfortunately it is unclear what else the NAs contain besides plants. Therefore, it cannot simply be assigned with out a laborious process. 
