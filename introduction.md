## In this analysis, we are trying to understand: 
>- How far from a park to apartments tend to be when they mention park in their listing?
>- Does the inclusion of a park in an apartment listing have a relationship to the listing price? Ie. do apartments that mention parks in their posts rent for higher than those that don't?

To get to the bottom of these questions, we scrapped craigslist posting, sorted for park mentions in the description, measured the distance between listings that mention parks and the nearest park, and compared prices of listings that mention parks and the median gross rent in their neighborhood. 

### STEP ONE: Scrapping
We scraped 9,000 apartment listings from craigslit in Los Angeles (on June 13, 2023) - see the "Scrapping" Notebook for more detail - and saved them in a dataframe called combined_df. This scrape pulled apartment descriptions and other relevant information like the location of the post (latitude and longitude) as well as the number of bedrooms, square footage, and number of bedrooms. 

### STEP TWO: Sorting
Next we filtered through the scrapping data to identify listings that mention parks. To do so, we looped through the listing descriptions marking them as "true" for parks mentioned if their description included the name of a park from a LA DataHub provided list of parks in LA County or a term like trails or hiking that alludes to a public park without naming the specific park. Once we deleted dupplicates and null values our 9,000 listings went down to around 7,500. Of those 7,500 roughly 20% included a mention of parks in the listing (1,450)

### STEP THREE: Distance Analysis
We went on to take a closer look at the distance between apartment listings that mentioned parks in their descriptions to the closest parks. Although we expected to see an increasing number of listings for smaller distances, the data showed that most listings were ground around 400 meters or a quarter mile from parks, and declined on either side of this distance. We visualized this relationship both in a map and a histogram. 

### STEP FOUR: Price Analysis
We went on to take a closer look at the apartments to identify any relationships between price of the apartment and the inclusion or absence of a park in the listing. To do so we grouped the apartments by census tract and found the average listing price for each tract as well as the average listing price for the apartments that include parks in their listing. 
