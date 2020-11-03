# A2: U.S. COVID Trends

## Overview
In many ways, we have come to understand the gravity and trends in the COVID-19 pandemic through quantitative means. Regardless of media source, people are consuming more epidemiological information than ever, primarily through reported figures, charts, and maps.

This assignment is your opportunity to work directly with the same data used by the New York Times. While the analysis is guided through a series of questions, it is your opportunity to use programming skills to ask more detailed questions about the pandemic.

You'll load the data directly from the [New York Times GitHub page](https://github.com/nytimes/covid-19-data/), and you should make sure to read through their documentation to understand the meaning of the datasets.

Note, this is a long assignment, meant to be completed over the two weeks when we'll be learning data wrangling skills. I strongly suggest that you **start early**, and approach it with patience. We're asking real questions of real data, and there is inherent trickiness involved.

## Analysis
You should start this assignment by opening up your `analysis.R` script. The script will guide you through an initial analysis of the data. Throughout the script, there are prompts labeled **Reflection**. Please write 1 - 2 sentences for each of these reflections below:

- What does each row in the data represent (hint: read the [documentation](https://github.com/nytimes/covid-19-data/)!)?
**Answer** Each row has separate columns that represent the date, location (country, state, or county), the number of COVID-19 cases, and another with the number of COVID-19 deaths.

- What did you learn about the dataset when you calculated the state with the lowest cases (and what does that tell you about testing your assumptions in a dataset)?
**Answer**  My assumption of cases in the state with the lowest cases were incorrect. I thought there would be much less than what was shown in the dataset. This tells me that I cannot just assume the amount of COVID-19 cases, without looking at the actual data.

- Is the location with the highest number of cases the location with the most deaths? If not, why do you believe that may be the case?
**Answer** The location with the highest number of cases (Los Angeles) is not the same as the location with the highest amount of deaths (New York) because COVID-19 does not directly equate to deaths. Things that need to be taken into consideration are the average age of the residents along with other personal health data that can link the causation between cases and deaths.

- What do the plots of cases and deaths tell us about the  pandemic happening in "waves"? How (and why, do you think) these plots look so different?
**Answer** The waves in the plot show us the trend of the number of reported cases and deaths. The sharp incline, then gradual decline represents the first wave in the reports of deaths. Since the first wave, the next two waves have not been as large, due to the fact that the potentiality that the reported cases are younger or “healthier” individuals that can recover from much easier.

- Why are there so many observations (counties) in the variable `lowest_in_each_state` (i.e., wouldn't you expect the number to be ~50)?
**Answer** It is possible for multiple counties to report a low number of cases, below 50 or even none.

- What surprised you the most throughout your analysis?
**Answer** I assumed that the total daily cases at the county and state levels would match the national total, but it did not on some dates. I thought that my R code was wrong when it reported 13 differences of data, but the numbers of counties/dates with differences was 15. It turns out that on one date, 2020-05-05, there was a +2 and -2 difference from two counties that cancelled the net effect out, and made it seem that the county aggregate total matched the national total on that date.
