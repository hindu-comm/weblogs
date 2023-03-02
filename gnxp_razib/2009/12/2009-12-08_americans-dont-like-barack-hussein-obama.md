+++
title = "\"Americans\" don't like"
full_title = "\"Americans\" don't like Barack Hussein Obama"
date = "2009-12-08"
upstream_url = "https://www.gnxp.com/WordPress/2009/12/08/americans-dont-like-barack-hussein-obama/"

+++
Source: [here](https://www.gnxp.com/WordPress/2009/12/08/americans-dont-like-barack-hussein-obama/).

"Americans" don't like Barack Hussein Obama

I post some data analysis over at [my other weblog](https://www.gnxp.com/blog/2009/12/food-stamps-unemployment-go-together.php). For example, today I looked at the relationship between [food stamp usage and unemployment](https://www.gnxp.com/blog/2009/12/food-stamps-unemployment-go-together.php). The Census makes a lot of county-level data available, though it’s often slapdash and disorganized. But using [R](http://www.r-project.org/) I’ve constructed many data sets including most American counties. I don’t post here much because I concentrate more on science in this space, and the 500 pixel width means that integrating scatter plots into a post seamlessly is pretty much impossible.  
But since [readers of this weblog](https://www.gnxp.com/blog/2009/02/gnxp-survey-results.php) are much more liberal than over at GNXP Classic, I thought you’d be interested in what demographic variables predict voting for Barack Obama on the county-level. So the dependent variable is the 2008 results for Barack Obama by county.  
The independent variables are:  
% of non-Hispanic whites who identify German  
% of non-Hispanic whites who identify as “American”  
% black  
% Median household income  
% Median home value  
% with a college degree  
% on food stamps  
% obese  
Below are the [coefficients](https://en.wikipedia.org/wiki/Standardized_coefficient) with errors and p-values if not significant).

  
% of non-Hispanic whites who identify German 0.13 (0.032)  
% of non-Hispanic whites who identify as “American” -0.89 (0.046)  
% black 0.20 (0.022)  
% Median household income \~ 0  
% Median home value \~ 0  
% with a college degree 0.33 (.037)  
% on food stamps 0.008 (0.0006)  
% obese -0.0012 (0.001, p-value 0.23)  
r-squared = 0.52  
I also calculated earlier [the white vote for Obama](https://www.gnxp.com/blog/2009/11/white-vote-for-obama-by-county.php) using a combination of county-level data and state-level exit polls. So here are the coefficients for prediction of the white vote for Obama:  
% of non-Hispanic whites who identify German 0.27 (0.026)  
% of non-Hispanic whites who identify as “American” -0.68 (0.045)  
% black -0.25 (0.023)  
% Median household income \~ 0  
% Median home value \~ 0  
% with a college degree -0.089 (.036)  
% of whites on food stamps 0.008 (0.0006)  
% obese -0.0037 (0.0092)  
r-squared = 0.56  
“Americans” are generally those of [British or Irish ancestry](https://en.wikipedia.org/wiki/British_American#2000_U.S_Census) who live in the South. The correlation between counties in their voting for Obama and % with a college degree = 0.38, and -0.42 for % who are “American” in ancestry. The sort of model above tries to control for other variables which are correlated together. When you control the other variables college degree % becomes less powerful as an independent effect in relation to the % who are “American.” Median house value (at least in 2005-2007) was correlated with the Obama vote at 0.33, but its effect goes to nothing when you control for other factors.  
**Note:** The r-squared represents the proportion of the variance in the dependent variable which can be explained by the independents.

### Related Posts:

- [Food stamps & unemployment go together
  (duh)](https://www.gnxp.com/WordPress/2009/12/08/food-stamps-unemployment-go-together-duh/) - [American data by
  counties](https://www.gnxp.com/WordPress/2009/11/29/american-data-by-counties/) - [Are over-leveraged counties seeing an increase in food
  stamp…](https://www.gnxp.com/WordPress/2009/11/29/are-over-leveraged-counties-seeing-an-increase-in-food-stamp-usage/) - [What's not the matter with
  Appalachia](https://www.gnxp.com/WordPress/2009/08/16/what-s-not-the-matter-with-appalachia/) - [The New York Times "pay
  wall"](https://www.gnxp.com/WordPress/2011/03/31/the-new-york-times-pay-wall/) - [Seed Magazine endorses Barack Hussein Obama
  II](https://www.gnxp.com/WordPress/2008/10/30/seed-magazine-endorses-barack-hussein-obama-ii/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F12%2F08%2Famericans-dont-like-barack-hussein-obama%2F&linkname=%22Americans%22%20don%27t%20like%20Barack%20Hussein%20Obama "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F12%2F08%2Famericans-dont-like-barack-hussein-obama%2F&linkname=%22Americans%22%20don%27t%20like%20Barack%20Hussein%20Obama "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F12%2F08%2Famericans-dont-like-barack-hussein-obama%2F&linkname=%22Americans%22%20don%27t%20like%20Barack%20Hussein%20Obama "Email")[](https://www.addtoany.com/share)
