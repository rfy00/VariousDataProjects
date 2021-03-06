<b><i>Intro</i></b> - Many people qualify for Social Security throughout the United States.  This project will utilize the dataset that was taken from data.world based on the “Annual report providing Social Security beneficiary population data by state and ZIP code. Report for 2015”.  The project will use various graphs and data tables to show how the data can be split up by ZIP code, County, City/Town, Number of Qualified Recipients, and Amount of Monthly Benefits (in thousands).  This will help answer whether there is a correlation between the Total Monthly Benefits and Total Number of Recipients.  It will also help answer questions about which Counties have the least and most amount of Total Monthly Benfits and Total Number of Recipients.  There were multiple datasets for all the U.S. but I only used the Arizona dataset.

<b><i>Tools</i></b> - R, R Markdown, HTML, Excel

<b><i>Data</i></b> - There is a total of 493 Arizona ZIP Code records and 14 variables in the dataset.  The dataset did not include the City/Town so I went on the Internet to find a list of ZIP Codes along with the City/Town and County.  I matched them up with the ZIP Codes in the original dataset.  The Social Security Administration mentions as a footnote in the dataset that "To avoid disclosing the reason for Social Security eligibility and amounts of benefits received, a controlled rounding procedure was used for field office and ZIP Code data.  Data are not shown for ZIP Codes with fewer than 15 beneficiaries".  Field Offices means U.S. Postal Service geographic areas.  The dataset includes Arizona ZIP Codes, Cities/Towns, Counties, total number of eligible beneficiaries, number of eligible retired works, number of eligible disabled workers, number of eligible widow(ers) and parents, number of eligible spouses, number of eligible children, all beneficiaries total monthly benefits (in thousands), retired workers total monthly benefits (in thousands), widow(ers) and parents total monthly benefits (in thousands), and number of OASDI (Old Age, Survivors and Disability Insurance). OASDI refers to payments made to eligible people in the United States that meet certain requirements.  After updating the spreadsheet (removing merged cells and overall total rows) and creating the oasdiData data frame in R, there was not a need to clean the data further.  There was a TotalMonthlyBenefits column that needed to be included as shown below.  The str function is used to show the structure and part of the information.

<b><i>Methods/Evaluation/Techniques</i></b> - I cleaned the data, summarized the various pieces of useful data, and used various statistical methods to evaluate the data.

<b><i>Conclusion</i></b> - Overall, depending on the groupings for the Total Number of recipient fields, the Top 5 varied a little by ZIP Code and City/Town.  For instance, Sun City and Sun City West are in Maricopa County and are retirement communities.  Surprise is just south of those communities so i would expect the number of total recipients to be high.  Tucson (second populous city in Arizona) and Green Valley (suburb of Tucson) are in Pima County (near the border in the South Quadrants) have the 4th and 5th highest recipients.

What was also interesting is all the cities/towns that were in the bottom 5 were in Apache County which is located in towards the northwest of Arizona next to the New Mexico border.  This may be due to population is not as high as other counties and Indian Reservations.

The correlation between the Number of recipients and the Monthly Benefits (in thousands) seem to be greater when the population is higher.  With Maricopa County being the most populous county and Pima County being the second most populous county, they will have more ZIP Codes that will be outliers compared to the rest of the state.

There were quite a few limitations that i ran into.  The dataset was mainly based on two major categories, Number of Recipients and Monthly Benefits.  There are only so many ways a person can slice and dice the data and look at it using graphs.  Looking at the other states where the same data was gathered for would help compare information.  A person would be able to gain better understanding of where the most people based on each category lived based on ZIP Code and County.  

<b><i>Navigation</i></b> - 

<b>Arizona OASDI Number of People Receiving Benefits.rmd</b> is the main R file

<b>Arizona OASDI Number of People Receiving Benefits and the Amount of Monthly Benefits.pdf</b> is the final output of the R Markdown code

<b>updateoasdi_zip15.xlsx</b> is the file that is uploaded into the rmd file

