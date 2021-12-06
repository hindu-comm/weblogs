+++
title = "Raking a Table"
full_title = "Raking a Table"
date = "2013-08-04"
upstream_url = "https://westhunt.wordpress.com/2013/08/04/raking-a-table/"

+++
Source: [here](https://westhunt.wordpress.com/2013/08/04/raking-a-table/).

Raking a Table

Thinking about preparing for a course this Fall, I had a look at the
current literature on assortative mating and found a pair of excellent
papers on assortment by education \[1,2\]. Using census data they
generated tables by decade from 1940 to 2000 with counts of marriages by
level of education of husband and wife. There are two families of tables
in these papers, one based on recent marriages (“newlyweds”) and the
other based on marriages of five or more years duration (“established”).
Since the established series is more up to date, I have looked at that
series.

Here is the raw data table from a sample from the 1940 US census of
established marriages. The data are given as percentages of the total
number of marriages but the raw numbers are simple to generate from the
published tables. Here for example is the data table from 1940:

                                                1940 Marriages
                                                Male Education
                                            <10     10-11    12     13-15    16+

                                <10         69729    7053    4945    1236     634 
                                10-11       11618    6150    4137    1093     570 
            Female              12          10382    5706   12887    3629    3027 
           Education            13-15        2092    1062    2330    2504    2567 
                                16+           507     253     745     855    2773 

The education categories are dated from today’s perspective: fewer than
ten years of schooling, ten to eleven years, high school graduate, some
college, and college graduate. Of course the significance of these has
changed since 1940: today’s associate degree is equivalent to finishing
high school in 1940 some would say. Nevertheless we can look at what we
have.

While the above table is complete, how do we make sense of it? Some
things are easy, for example the largest number of marriages, 69729,
were those in which both partners had fewer than ten years of education.
In 2000 the largest number of established marriages is between two
college graduates. The smallest entry in 1940, 507, is for college
graduate women married to men with fewer than ten years of schooling.
Interesting numbers, I suppose, but what is the big picture? Is there a
little or a lot of assortative mating? For a full analysis using
log-linear models and covariates see the above papers. The second, by
Schwartz and Mare, is well written, easy to understand, but it is a full
course meal. What I want is a snack, a tasty cracker, rather than a full
meal.

One attractive approach to generating a light snack is called “raking”
the table \[3\]. This technique was a hot topic way back when I was in
graduate school \[4\]. Iterating, one adusts the marginals, alternating
rows and columns, to some desired values. In more detail: first compute
the column sums, then divide each column by its sum, then sum the rows,
then divide each row but its sum, repeating these steps until the table
stops changing. This adjusts the marginals, i.e. the row and column
sums, to 1.

This method, applied to the 1940 marriages, gives this:

                                            1940 Marriages
                                      0.59  0.23  0.12  0.04  0.02
                                      0.23  0.42  0.25  0.08  0.02
                                      0.11  0.23  0.36  0.22  0.08
                                      0.04  0.08  0.19  0.41  0.28
                                      0.03  0.03  0.09  0.25  0.60

The row and column labels are the same as in the table above. What do
these numbers mean? They are (supposed to be) estimates of what we might
call “attraction.” (I want to say “preference” but sociologists use that
for something else.) Since we have iterated to unit marginals (the rows
and columns each sum to unity), the numbers tell us how many marriages
of each mating-type (pair of education levels) would occur if the
numbers of potential mates from each level were the same. For example,
the rows correspond to female partners. The second entry in the first
row, 0.23, tells us that if the mating pool numbers were uniform across
levels, 23% of the women with fewer than ten years of schooling would
marry men with ten or eleven years of schooling. We could have adjusted
the marginals to anything we wished, of course, but the reduction to
unit marginals in my opinion gives the simplest picture possible of
assortative mating by education.

Here is the same table from the 2000 census:

                                              2000 Marriages
                                        0.64  0.19  0.11  0.05  0.02
                                        0.19  0.48  0.21  0.09  0.02
                                        0.11  0.21  0.39  0.22  0.08
                                        0.04  0.1   0.22  0.42  0.21
                                        0.01  0.02  0.08  0.22  0.67

Now things are starting to get strange. The diagonals in the 2000 table
are slightly greater, indicating more within-group marriage attraction,
but not much. Other than that is is essentially the same table. Hardly
anything has changed in 60 years!

Here is another (to me) surprise. Female hypergamy (marrying up) is
often thought to be common. A simple indicator is the average number of
marriages in the upper triangle (male education>female), on the diagonal
(both partners have same education level), and in the lower
triangle(male education\<female). There is scarcely any indication of
preferential hypergyny, neither in 1940 nor in 2000 nor in the intervals
between. There might be some if I had reported more signficant digits
but it would not be large enough to be of any interest.

                            Average of upper triangle, diagonal, and lower triangle values

                                 Year   Female<Male    Same        Female<Male

                                 1940       0.37       0.47           0.37
                                 1960       0.37       0.48           0.37
                                 1980       0.38       0.50           0.37
                                 2000       0.38       0.52           0.38

So this is the cracker I have gotten ready for my class this fall,
perhaps 15 minutes worth. If you are interested in digging deeper I
recommend a careful read of Schwartz and Mare \[2\]: good luck.

If you are interested in the numbers, here are the raw data straight
from their paper, in a format such that you can copy one of the blocks
and read it directly as a floating point array with numeric python’s
loadtxt() function.

    # year 1940 counts from schwartz and mare 2005 demography
    # men in columns, women in rows, schooling increases across and down
    #N=158512
    28.83   4.37   3.53   0.62 0.42   
    7.23    4.96   4.67   0.72 0.22   
    7.01    5.80   14.29  3.92 2.30   
    0.74    0.52   1.97   1.97 2.05   
    0.25    0.12   0.52   0.64 2.32   

    #1960
    #N=203117
    9.32  2.94  2.85  0.47 0.19 
    4.70  5.04  6.94  1.42 0.37 
    5.84  6.41  22.61 6.93 3.01 
    0.63  0.76  3.35  5.15 3.81 
    0.10  0.08  0.84  1.54 4.69 

    #1980
    #N=239980
    2.68   1.51   1.92   0.44  0.09   
    1.51   3.16   5.00   0.94  0.16   
    2.23   4.33   25.51  8.26  3.03   
    0.42   1.03   7.08   9.48  5.51   
    0.09   0.14   1.66   3.37  10.46  

    #2000
    #N=220209
    3.47  0.60  1.42 0.52  0.16
    0.68  1.01  1.79 0.65  0.13
    1.80  2.02  15.54 7.33  2.41  
    0.76  1.06  9.26 14.91  6.98
    0.17  0.18  2.80 6.33  18.02 

REFERENCES

\[1\] R.D. Mare, Five decades of educational assortative mating,
American Sociological Review. (1991) 15–32.

\[2\] C.R. Schwartz, R.D. Mare, Trends in educational assortative
marriage from 1940 to 2003, Demography. 42 (2005) 621–646.

\[3\] A. Agresti, Categorical data analysis, Wiley, Hoboken, NJ, 2013.

\[4\] F. Mosteller, Association and estimation in contingency tables,
Journal of the American Statistical Association. 63 (1968) 1–28.

