# Prosper Loan Data
## by Paul Seo


## Dataset

This data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others. Before I started my exploratory visual investigations, I trimmed the dataframe down to 14 variables I would like to work with. Not all of them were part of my analysis. One other wrangling procedure I conducted before analysis was that of regarindg loan terms. At face value loan terms seemed numerical, but there were only 3 types of loan terms in the dataset, 12, 36, and 60 months. I converted these to string objects so that my plots would treat them as categorical variables. One other wrangling step I took was during the visualization I found that exact credit scores of borrowers were not listed, but instead their lower and upper limits. I worked with upper limits and simulated a real credit score by adding some jitter to the plot. You can see this at work in my final multivariate plot.

## Summary of Findings

I used bar chart to look at the count of different loan terms. 36 months (3 years) loans dominate as the primary loan type. Significantly less, but 60 months (5 years) loan term comes in 2nd and lastly 12 months (1 year). We should definitely look into if there is relationship between loan terms and loan amounts in the next section.

I used histogram to look at the distribution of loan amounts. The distribution of loan amount is right-skewed, with a majority of borrowers borrowing under $10,000.

I used a bar chart to find out how many of the borrowers were home owners and how many were not. There seems to be almost a 50:50 split between homeowner status.

I used histogram to take a look at the distribution of credit scores. Credit score looks to be normally distributed as expected, but there is an important takeaway here with the fact that it seems harder to climb in credit score after reaching around ~700 as compared to reaching 700.

I used histogram to take a look at the distribution of loan interest rates. Seems normally distributed centered around 15%, but there's a big spike at 30%. 15% and 30% may be the most common interest rate out there for loans.

I used scatterplot to see relationship between Interest Rate and Loan Amount. We can clearly see the negative correlation Loan Amount has with the interest rate. While smaller loans ( < 10000) are capping out at 35% interest rate, borrowing 35k is only capping at around 15%. In betweemn you can see this downward trend very clearly. In fact, the highest amount of interest for someone borrowing 35k is 18.19%.

I used box plot to see the relationship between Loan Amount and Loan Terms. Much to my surprise, the loan term and interest rate have a slight positive correltion. This may have been caused by the fact that longer loan terms are usually issued for bigger loans and hence interest rate staying relatively similar to a smaller loan with shorter terms. To verify this we may have to conduct a multivarite visualization including loan amount.

I used clustered bar chart to see the relationship between Loan Terms and status of a homeowner. A very interesting insight is found. We see that for both 12 and 37 month term loans, there's an approximate 50:50 split on borrowers being a homeowner or not. However, when we go to loans that are borrowed for 60 terms, we see that there are way more homeowners than those who do not own any homes. I would like to believe that this is because owning a home comes with the benefit of having less debt, hence the ability to afford long loan terms.

I used clustered bar chart again to see the relationship between Employment Status and Homwowner status. Indeed we see that among those who are employed, more people are homeowners than those who are not.

I used a faceted plot to see the relationship between Loan Terms, Loan Amount, and Interest Rate. A few very interesting insights can be gained here. First, 12 month term loans have the lowest interest rate and is by far the least occuring loan term. The highest recorded 12 month term loan was also 25k. Secondly, we see that based on the frequency of dots on the general graph, 36 term loans are the most frequent - and it only makes sense that the loaners try to make their most money from this group of borrowers by charging them the highest interest across all loans. Across all loan amounts up to 30k, we see that 36 month term loans have the highest interest rates. In the last graph, we see that 60 month loans are the second-most popular loan type. They generally offer a lower interest across the board, except bigger loans, starting at 30k and up, with marginal increase in interest rates.

Finally, I used faceted plot once again to see the relationship between Loan Terms, Credit Score, and Interest Rate. Two interesting insights from this plot: First, we see that there is a moderate negative correlation between Credit Score and Interest Rate. The higher your credit score, the more you are rewarded with less interest. Makes sense. Secondly, we see that longer term loans (60 months) with generally higher committment and shorter term loans with generally higher payments (12 months) are only given to borrowers with higher credit score (> 600). Meanwhile, we see that borrowers with lower than 600 credit score are often finding themselves with 36 month term loans.


## Key Insights for Presentation

I implemented 3 of my plots from the previous section to put in my presentation: Loan Amounts histogram, Loan amounts vs. Interest Rate scatterplot, and Faceted plot (Loan Term, Interest Rate, and Loan Amount).

For each of these I added proper labels and titles for the plots. For the scatterplot and the faceted scatterplot, I added alpha of 0.05 to compensate for more than 100k points being plotted to better capture the frequency of each of loan terms.
