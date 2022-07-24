# (Loan Data From Prosper)
## by (Mariam Fayena)


## Dataset

 This data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others.
>  [ All column information](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0)


## Preliminary Wrangling
out of the 81 columns i choosed the data set i would focus on into a data fram which includes
* ListingNumber: The number that uniquely identifies the listing to the public as displayed on the website.
* Term: The length of the loan expressed in months.	
* LoanStatus: The current status of the loan: Cancelled,  Chargedoff, Completed, Current, Defaulted, FinalPaymentInProgress, PastDue. The PastDue status will be accompanied by a delinquency bucket.
* BorrowerAPR: The Borrower's Annual Percentage Rate (APR) for the loan.
* BorrowerRate: The Borrower's interest rate for this loan.
* ProsperRating: The Prosper Rating assigned at the time the listing was created between AA - HR.  Applicable for loans originated after July 2009.	
* ProsperScore: A custom risk score built using historical Prosper data. The score ranges from 1-10, with 10 being the best, or lowest risk score.  Applicable for loans originated after July 2009.
* BorrowerState:The two letter abbreviation of the state of the address of the borrower at the time the Listing was created.
* Occupation: The Occupation selected by the Borrower at the time they created the listing.
* EmploymentStatus:The employment status of the borrower at the time they posted the listing.
* IsBorrowerHomeowner: A Borrower will be classified as a homowner if they have a mortgage on their credit profile or provide documentation confirming they are a homeowner.
* IncomeRange: The income range of the borrower at the time the listing was created.
* LoanOriginalAmount: The origination amount of the loan.
* LoanOriginationDate: The date the loan was originated.
* Listing_category: The category of the listing that the borrower selected when posting their listing

#### Wrangling
changed the Loan Origination Date into a date time category
created a better representation of the Listing category


## Summary of Findings

### Univariate Exploration

In the exploration, I found that there was a strong relationship between the betweem borrowers APR and borrowers rate.they had the same plot pattern. which is normal because Borrower Rate pluse other charges make up the Borrower APR.
The loan amount collected was widely distributed, between 1000 and slight above 30000 dollars.
the prosper Score distrbution  showed that it is multimodal, with score 4,6,8 dominaing the population
Prosper Rating distribution showed C was the most common rating among the borrowers and the least population had the highest rating which was AA.
The employment status distribution depict majority of individuals that applied for the loans are employed and the least being retired individuals.
The homeowners distribution was evenly distributed in the population.
Large numbers of the borrowers are of the high income range earners.
using the log scale, the borrowers who are currently on the loan plan are the highest, followed by those who have completed the loan
Majority of the loan was collected for debt consolidation.

### Bivariate Exploration
Using a bar plot to get the average borrower APR distribution by year, it depict that 2011 had the highest APR. creating the distribution by month with a line plot indicated september has the overall APR mean value.However creating the APR distribution by month showed that month with lower APR saw larger amount of individuals collecting loans.

Using a bar plot to depict the relationship between prosper rating and score shows that the higher the borrower APR the lower the prosper ratings and scores. This is a major finding which will be documented in my Expanatory Analysis. 

Using a correlation heatmap to show relationship between Borrower APR,Rate,Loan amount and Prosper Score it shows higher correlation between the borrower APR and rating and a negative relationship between prosper score and API confirming the box plot above.

Using a heatmap to show the relationship Between Income Range and Homeowner, The distribution show that majority of the individals collect loans within 10k range below. Also,within 15k above the borrowers who had homes dominated the disribution in collecting higher loans range

using clusterd bar chart to show the Loan amount been distributed by the Term, The plot shows that 36 term which is 3 years was the highest distribution for all the amount collected except for the 30k upward, which had the 60 term that 5 years slightly higher. Only a few borrowers collected loans for one year, and for the higher loan from 25k no individual collected the loan for a year.

### Multivariate Exploration
Showing how  Borrower APR affect the loan range and  Homeowner relationship with an heatmap to look further into the bivariiate plot, the disribution shows that The borrowers APR had no effect on the home owner relationship. Although, the loan amount had an inverse relationship with borrower APR.

Looking further into the clusterd bar chart in the bivariate while adding Term to the distribution, the plot shows that the longer term(5 years) had higher borrower APR. which means the longer the term the individual collect the loan the higher their API gets.

the two multivariate insight are significant for my explainatory analysis.

## Key Insights for Presentation

The first multivariate showed that the higher the API, the lower the loan collected and the homeowner had no influence on the loan amount range. However, using the term shows the longer the term which loan was collected no matter the amount, the higher the APR gets.

