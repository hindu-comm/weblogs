+++
title = "How income, class,"
full_title = "How income, class, religion, etc relate to political party"
date = "2012-03-26"
upstream_url = "https://www.gnxp.com/WordPress/2012/03/26/how-income-class-religion-etc-relate-to-political-party/"

+++
Source: [here](https://www.gnxp.com/WordPress/2012/03/26/how-income-class-religion-etc-relate-to-political-party/).

How income, class, religion, etc. relate to political party

**Update:** There was a major coding error. I’ve rerun the analysis. No qualitative change.

As is often the case a 10 minute post using the [General Social Survey](http://sda.berkeley.edu/cgi-bin/hsda?harcsda+gss10) is getting a lot ofattention. Apparently circa 1997 web interfaces are so intimidating to people that extracting a little data goes a long way. Instead of talking and commenting I thought as an exercise I would go further, and also be precise about my methodology so that people could replicate it (hint: this is a chance for readers to follow up and figure something out on their own, instead of tossing out an opinion I don’t care about).



Just like below I limited the sample to non-Hispanic whites after the year 2000. Here’s how I did it:YEAR(2000-\*), RACE(1), HISPANIC(1)

Next I want to compare income, with 1986 values as a base, with party identification. To increase sample sizes I combined all Democrats and Republicans into one class; the social science points to the reality that the vast majority of independents who “lean” in one direction are actually usually reliable voters for that party. So I feel no guilt about this. I suppose Americans simply like the conceit of being independent? I know I do. In any case, here are the queries:

For row: REALINC(r:0-20000″LLM”;20000-40000″M”;40000-80000″UM”;80000-\*”BU”)  
For column: PARTY(r:0-2″Dem”;3″Ind”;4-6″Rep”)

What I’m doing above is combining classes, and also labeling. The GSS has documentation to make sense of it if you care. Some of you were a little confused as to what \$80,000 household income in 1986 means. I went and converted 1986 dollars to dollars today.

|                                |           |
|--------------------------------|-----------|
| **Value of income conversion** |           |
| *1986*                         | *2012*    |
| \$20,000                       | \$42,000  |
| \$40,000                       | \$83,000  |
| \$80,000                       | \$166,000 |



As you can see \$80,000 in 1986 would be \$166,000 today. So what percentile in household income is \$166,000? Here it is (I rounded generously, so it is really 43 or 93 and such, instead of 40 or 95):

|                      |                        |                            |
|----------------------|------------------------|----------------------------|
| **Income range**     | **Quantitative class** | **Descriptive class**      |
| Up to \$20,000       | \< 40%                 | Lower & Lower Middle (LLM) |
| \$20,000 to \$40,000 | 40% to 70%             | Middle (M)                 |
| \$40,000 to \$80,000 | 70% to 95%             | Upper Middle (UM)          |
| \$80,000 and up      | \> 95%                 | Broad Upper (BU)           |

To clear up future confusions I have relabeled the income ranges with the descriptive classes above. You can argue all you want that being in the \~5% of income is not upper class, but just pretend I used a different term (e.g., higher middle class?). I’m not too hung up on the terminology, I’m more focused on the people in the top 5% of the income distribution. The local doctor or successful business person, not the billionaire who owns an island in the Caribbean.

Now you have a sense of the classes which we’ll be looking at. In the results below I report the proportions of the row and column values. So the leftmost three columns will tell you the percentage of Democrats who are upper class, while the rightmost three columns will tell you the percentage of upper class people who are Democrats. The leftmost three columns add up to 100% vertically, the rightmost three columns 100% horizontally.

The second major aspect of reading the table below is that I “controlled” for various sets of characteristics. So, for example, you see the income and party identification patterns for those with no college education, and those with college educations. Here are the variables:

DEGREE(r:0-2″No College”;3-4″College”), BIBLE,REGION(r:1-4,8-9″Not South”;5-7″South”), SEI

Two notes here. First, I used the Census [division categories](http://www.census.gov/geo/www/reg_div.txt). Second, the “socioeconomic status index” is more than just income, and I created three broad classes, giving you the percentile ranges.

------------------------------------------------------------------------

|                                    |                |     |     |     |             |     |     |
|:-----------------------------------|:---------------|:----|:----|:----|:------------|:----|:----|
|                                    |                |     |     |     |             |     |     |
|                                    | Columns = 100% |     |     |     | Rows = 100% |     |     |
|                                    | Dem            | Ind | Rep |     | Dem         | Ind | Rep |
| LLM                                | 42             | 51  | 33  |     | 40          | 24  | 33  |
| M                                  | 28             | 27  | 28  |     | 37          | 18  | 45  |
| UM                                 | 21             | 16  | 27  |     | 35          | 13  | 53  |
| BU                                 | 8              | 6   | 11  |     | 34          | 11  | 55  |
|                                    |                |     |     |     |             |     |     |
| No College                         |                |     |     |     |             |     |     |
|                                    | Dem            | Ind | Rep |     | Dem         | Ind | Rep |
| LLM                                | 51             | 55  | 39  |     | 39          | 26  | 35  |
| M                                  | 29             | 27  | 31  |     | 36          | 20  | 44  | | UM                                 | 16             | 14  | 24  |     | 31          | 16  | 53  | | BU                                 | 4              | 3   | 6   |     | 28          | 15  | 57  | |                                    |                |     |     |     |             |     |     | | College                            |                |     |     |     |             |     |     | |                                    | Dem            | Ind | Rep |     | Dem         | Ind | Rep | | LLM                                | 24             | 28  | 19  |     | 45          | 13  | 42  | | M                                  | 25             | 28  | 24  |     | 42          | 11  | 47  | | UM                                 | 32             | 25  | 35  |     | 40          | 8   | 35  | | BU                                 | 19             | 19  | 22  |     | 38          | 9   | 53  | |                                    |                |     |     |     |             |     |     | | Bible is Word of God               |                |     |     |     |             |     |     | |                                    | Dem            | Ind | Rep |     | Dem         | Ind | Rep | | LLM                                | 63             | 61  | 39  |     | 35          | 22  | 44  | | M                                  | 27             | 28  | 32  |     | 24          | 16  | 59  | | UM                                 | 10             | 10  | 23  |     | 16          | 10  | 75  | | BU                                 | 1              | 2   | 5   |     | 7           | 11  | 82  | |                                    |                |     |     |     |             |     |     | | Bible is Inspired of God           |                |     |     |     |             |     |     | |                                    | Dem            | Ind | Rep |     | Dem         | Ind | Rep | | LLM                                | 37             | 49  | 28  |     | 41          | 23  | 36  | | M                                  | 31             | 29  | 29  |     | 41          | 16  | 43  | | UM                                 | 24             | 17  | 29  |     | 37          | 11  | 52  | | BU                                 | 8              | 5   | 14  |     | 30          | 8   | 62  | |                                    |                |     |     |     |             |     |     | | Bible is Book of Fables            |                |     |     |     |             |     |     | |                                    | Dem            | Ind | Rep |     | Dem         | Ind | Rep | | LLM                                | 37             | 51  | 28  |     | 51          | 29  | 28  | | M                                  | 25             | 22  | 24  |     | 53          | 20  | 24  | | UM                                 | 23             | 20  | 30  |     | 50          | 17  | 30  | | BU                                 | 15             | 7   | 18  |     | 55          | 11  | 34  | |                                    |                |     |     |     |             |     |     | | Not the South                      |                |     |     |     |             |     |     | |                                    | Dem            | Ind | Rep |     | Dem         | Ind | Rep | | LLM                                | 40             | 50  | 28  |     | 41          | 24  | 35  | | M                                  | 27             | 27  | 28  |     | 39          | 18  | 43  | | UM                                 | 23             | 17  | 28  |     | 38          | 13  | 49  | | BU                                 | 10             | 6   | 11  |     | 39          | 12  | 49  | |                                    |                |     |     |     |             |     |     | | The South                          |                |     |     |     |             |     |     | |                                    | Dem            | Ind | Rep |     | Dem         | Ind | Rep | | LLM                                | 47             | 54  | 33  |     | 39          | 23  | 33  | | M                                  | 29             | 28  | 29  |     | 35          | 17  | 48  | | UM                                 | 18             | 14  | 27  |     | 28          | 11  | 60  | | BU                                 | 6              | 4   | 12  |     | 23          | 9   | 67  | |                                    |                |     |     |     |             |     |     | | Bottom 50% of socioeconomic status |                |     |     |     |             |     |     | |                                    | Dem            | Ind | Rep |     | Dem         | Ind | Rep | | LLM                                | 55             | 59  | 44  |     | 40          | 27  | 33  | | M                                  | 28             | 27  | 30  |     | 36          | 23  | 41  | | UM                                 | 14             | 11  | 21  |     | 32          | 17  | 51  | | BU                                 | 4              | 3   | 5   |     | 34          | 17  | 49  | |                                    |                |     |     |     |             |     |     | | 40% to 10% of socioeconomic status |                |     |     |     |             |     |     | |                                    | Dem            | Ind | Rep |     | Dem         | Ind | Rep | | LLM                                | 34             | 38  | 26  |     | 40          | 19  | 41  | | M                                  | 31             | 30  | 29  |     | 38          | 14  | 47  | | UM                                 | 26             | 24  | 31  |     | 33          | 13  | 54  | | BU                                 | 9              | 7   | 15  |     | 28          | 10  | 62  | |                                    |                |     |     |     |             |     |     | | Top 10% of socioeconomic status    |                |     |     |     |             |     |     | |                                    | Dem            | Ind | Rep |     | Dem         | Ind | Rep | | LLM                                | 18             | 28  | 17  |     | 43          | 14  | 43  | | M                                  | 24             | 27  | 24  |     | 41          | 11  | 48  | | UM                                 | 30             | 20  | 34  |     | 40          | 6   | 53  | | BU                                 | 26             | 25  | 25  |     | 42          | 9   | 48  | |                                    |                |     |     |     |             |     |     |

### Related Posts:

- [Using the General Social
  Survey](https://www.gnxp.com/WordPress/2010/07/08/using-the-general-social-survey/) - [New comment
  format](https://www.gnxp.com/WordPress/2009/12/27/new-comment-format/) - [2014 Gene Expression reader
  survey](https://www.gnxp.com/WordPress/2014/11/13/2014-gene-expression-reader-survey/) - [The Onion on data
  overload](https://www.gnxp.com/WordPress/2009/05/19/the-onion-on-data-overload/) - [Accelerated human evolution in non-coding
  regions?](https://www.gnxp.com/WordPress/2006/11/02/accelerated-human-evolution-in-non-coding-regions/) - [Republicans, the middle class
  party](https://www.gnxp.com/WordPress/2010/08/06/republicans-the-middle-class-party/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F03%2F26%2Fhow-income-class-religion-etc-relate-to-political-party%2F&linkname=How%20income%2C%20class%2C%20religion%2C%20etc.%20relate%20to%20political%20party "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F03%2F26%2Fhow-income-class-religion-etc-relate-to-political-party%2F&linkname=How%20income%2C%20class%2C%20religion%2C%20etc.%20relate%20to%20political%20party "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2012%2F03%2F26%2Fhow-income-class-religion-etc-relate-to-political-party%2F&linkname=How%20income%2C%20class%2C%20religion%2C%20etc.%20relate%20to%20political%20party "Email")[](https://www.addtoany.com/share)
