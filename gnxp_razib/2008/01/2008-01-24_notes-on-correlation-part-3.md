+++
title = "Notes on Correlation"
full_title = "Notes on Correlation Part 3"
date = "2008-01-24"
upstream_url = "https://www.gnxp.com/WordPress/2008/01/24/notes-on-correlation-part-3/"

+++
Source: [here](https://www.gnxp.com/WordPress/2008/01/24/notes-on-correlation-part-3/).

Notes on Correlation: Part 3

I’m sure you have been waiting with bated breath (not!) for the final part of these notes.

Part 1 is [here](https://www.gnxp.com/blog/2007/09/notes-on-correlation-part-1.php) and Part 2 [here](https://www.gnxp.com/blog/2007/11/notes-on-correlation-part-2.php).

This final part deals with the basics of multivariate correlation and regression, that is, correlation and regression involving more than two variables. Multivariate correlation and regression are among the most commonly used tools in psychology and the social sciences, so it seems desirable to acquire some basic knowledge of the methods and their pitfalls.

I emphasise again that these notes are not aimed at expert statisticians, but at anyone who wants or needs a treatment of the subject using only elementary mathematics. I do not claim that there is anything original in the notes, but I believe that Part 3 brings together some material not easily found in any single source.

Most of Part 3 was written several months ago. I have tinkered with it at intervals since then, in an effort to make it more readable and intelligible, but without much success. I am posting it now (below the fold) as I doubt that I can improve on it, and I might as well get it out of the way.

I have only used non-mathematical typography, so on the remote chance that anyone wants to study the notes at leisure, they should be able to paste and save them in any WP program.

**Multivariate Correlation and Regression**  
**Preliminaries**

These notes avoid using special mathematical symbols, because Greek letters, subscripts, etc, may not be readable in some browsers, or even if they are readable may not be printable. As in previous parts, S stands for ‘sum of’, s stands for ‘standard deviation of’, ^2 stands for ‘squared’, and \# stands for ‘square root of’. All variables represent deviation values unless otherwise stated. The notation used for correlation and regression will be the same as in Part 2, with the following modifications.

In dealing with multivariate correlation and regression, the relevant variables are conventionally indicated by subscripts. For example, the partial correlation coefficient between x and y, taking account of z, would usually be indicated by the symbol ‘r’ for correlation followed by subscripts ‘xy.z’. Since I cannot use subscripts, I will adopt the following conventions:

– the notation for bivariate (2-variable) correlation and regression coefficients will be as in Part 2.

– multivariate correlation and regression coefficients will be indicated by upper-case letters: R for correlation and B for regression, to contrast with lower-case r and b for the bivariate coefficients. It should therefore be possible to tell at a glance whether the coefficients are bivariate or multivariate.

– the letters immediately following R or B are to be interpreted as subscripts.

– to avoid ambiguity, the letters used to stand for variables other than subscripts will be shown in upper case. For example, Rxy.z.Y indicates the variable Y, multiplied by the partial correlation coefficient between X and Y, given Z.

– where a correlation or regression coefficient is squared, the ‘squared’ symbol ^2 will follow any ‘subscripts’. E.g. Rxy.z^2 will indicate the square of the partial correlation coefficient Rxy.z.

I am aware that this notation is not easy to read, and sometimes produces ugly strings of upper-case letters, but after toying with various alternatives I find it the least-worst approach.

For (relative) simplicity I will deal mainly with the case of three variables, as this illustrates all the essential points. Suppose there are three sets of items, represented by the variables X, Y and Z, each set containing N items with numerical values. We assume that the items in each set are in a one-to-one correspondence (mapping) of some kind with the items of each other set. As with the bivariate case, there could be different ways of mapping the items onto each other. Correlation and regression are always relative to some intended system of mappings. The multivariate case does however raise a new potential complication. We can trace a mapping between any two of the variables either directly or indirectly, e.g. directly from X to Z, or indirectly from X through Y to Z. But are the resulting mappings from X to Z necessarily the same? Are the same X items always matched with the same Z items, whether directly or indirectly? It is not logically necessary that the mappings should be unique, and authors are sometimes vague on this point, but the intention is evidently that they are unique. If each item were indexed with a subscript from 1 to N, the intended correlations and regressions would always those between items with matching subscripts. Subscripts of this kind should be taken as implied.

**Aims of Multivariate Analysis**

There are two main reasons for going beyond the bivariate (2-variable) case to consider systems of more than two variables. First, we may hope to get a better estimate or prediction of the value of a variable if we make use of information about more than one other related variable. Second, the relationships between variables may not be fully understood if we only consider them on a pair-by-pair basis. For example, it may be that the correlation between two variables is affected by their correlations with a third variable.

These considerations lead to two seemingly distinct problems. First, what is the best way of predicting the value of a variable given the values of two or more other variables? Second, how can we separate and quantify the role of each variable independently of the others? These two problems turn out to be closely related.

**The problem of prediction**

The cases of interest for analysis arise where there are at least two non-zero correlations. Suppose for example that we have variables X, Y, and Z, and non-zero correlations rxz and ryz. For simplicity suppose also that all three variables have the same standard deviations, so that the correlation coefficients are equal to the regression coefficients. With these assumptions we can predict that a deviation of A in X will on average be associated with a deviation of rxz.A in Z. Similarly a deviation of A in Y will be associated with a deviation of ryz.A in Z. But what prediction should we make if we know the deviations in both X and Y?

In two special cases we can make a plausible guess. If X and Y are themselves perfectly correlated (rxy = 1), then a deviation of A in X always corresponds to a deviation of A in Y, and vice versa (still assuming equal standard deviations). It follows from this (and the assumed uniqueness of mappings) that rxz = ryz, since corresponding pairs of XZ and YZ products will have the same value, and the covariances, correlations, and regressions derived from these products will be equal. The X and Y values will therefore each give the same prediction of Z. So far as their correlations with Z are concerned, we might regard X and Y as being merely different names for the same entity. A knowledge of the value of Y gives us no new information if we already know the value of X, and vice versa. We would therefore not expect the correlation between Y and Z to help us predict the value of Z more accurately than we can already predict from the correlation between X and Z, and it is plausible that the ‘best estimate’ of Z, given X and Y, is the same as the estimate based on X or Y alone.

At the other extreme, suppose the correlation between X and Y is zero. In this case a knowledge of the value of X gives us no information at all about the value of Y. It is therefore reasonable to expect that the predictive value of Y will be entirely additional to that of X, and it is plau  
sible that the ‘best estimate’ of Z, given X and Y, will be the sum of the estimates based on X and Y, giving Z = rxz.X + ryz.Y.

But these are not rigorous proofs, and they give us little help in dealing with the majority of cases, where the correlation between X and Y is neither zero nor perfect. Here, we can only vaguely expect that the predicted value of Z, given X and Y, will be somewhere between the values predicted for the two extreme cases. For anything more precise, we need a more sophisticated approach. This is given by the theory of multiple regression.

**Multiple Regression**

The theory of linear regression and correlation based on the method of least squares (see Parts 1 and 2) can be extended to more than two variables. In the 2-variable (bivariate) case we wished to estimate the value of one variable, X, given the value of the other variable, Y. In the extension of the theory we wish to estimate the value of X given the value of two or more other variables, Y, Z, etc. The variable whose value we wish to estimate is usually called the dependent variable, and the others the independent variables, but these terms do not imply a direct causal relationship between them, or that if there is a casual relationship the causation runs from the independent to the dependent variable. ‘Dependent’ is merely a conventional term to designate the term whose value we want to estimate.

The key assumption of the method is that the estimate can be made in the form X = a + bY + cZ…., where there are no terms of the form YZ, involving more than one of the independent variables, and no squares or higher powers. This is a linear multiple regression equation, and the terms b, c, etc are called partial regression coefficients. Taking X as the dependent variable (the one whose value we wish to estimate), the partial regression coefficients will be designated Bxy.z and Bxz.y, which may be read as ‘the regression coefficient of X on Y, given Z’ and ‘the regression coefficient of X on Z, given Y’. With this notation, the multiple regression equation for the estimate is X = a + Bxy.z.Y + Bxz.y.Z. For the time being we cannot assume that the partial regression coefficients have any meaning in isolation from this equation.

To obtain the ‘best’ estimate, in accordance with the method of least squares (see Part 1), we need to find the values of the constant a, and the coefficients Bxy.z, and Bxz.y, for which S(X – a – Bxy.z.Y – Bxz.y.Z)^2 is at a minimum. Using the same methods as in the bivariate case (see Part 2), S(X – a – Bxy.z.Y – Bxz.y.Z)^2 can be treated as a function of each coefficient in turn, and we can derive an equation for each coefficient, in which the first derivative (strictly, partial derivative) of the function is equated to zero to find its minimum value. The only difference from the bivariate case is that the unknown value of the other coefficient appears in the resulting equation for each coefficient. We therefore do not immediately get a single solution, but a set of simultaneous equations with one equation for each coefficient. Since there are as many equations as unknowns, these equations can be solved by standard methods (determinants, etc).

As in the bivariate case, it can be shown that if all the variables are expressed as deviation values, the constant, a, must be zero. Assuming this proved, to find the coefficients Bxy.z, and Bxz.y themselves we therefore need to find the values for which S(X – Bxy.z.Y – Bxz.y.Z)^2 is at a minimum. Treating this as a function of Bxy.z and Bxz.y in turn, and equating the first derivatives to zero, we get the two equations:

SXY – Bxy.z.SY^2 – Bxz.y.SYZ = 0

SXZ – Bxz.y.SZ^2 – Bxy.z.SYZ = 0

These simultaneous equations can be solved by high school algebra to give:

Bxy.z = (SXY.SZ^2 – SXZ.SYZ)/(SY^2.SZ^2 – SYZ.SYZ)

Bxz.y = (SXZ.SY^2 – SXY.SYZ)/(SY^2.SZ^2 – SYZ.SYZ)

These coefficients can be given a more attractive form if the numerator and denominator are both divided by an appropriate factor. For example, if the first coefficient is divided through by SY^2.SZ^2, we get an expression equivalent to:

Bxy.z = (bxy – bxz.bzy)/(1 – byz.bzy)

where bxy, etc, are bivariate regression coefficients. If all the bivariate coefficients are already known, the partial regression coefficients may therefore easily be calculated. It may be noted that byz.bzy = ryz^2, so the denominator can also be expressed in the form (1 – ryz^2).

Using the same methods, Bxz.y comes out as (bxz – bxy.byz)/(1 – bzy.byz).

We have treated X as the dependent variable, but any of the other variables could also be treated as dependent, and appropriate partial regression coefficients calculated. For example, Byx.z comes out as (byx – byz.bzx)/(1 – bxz.bzx).

With the partial regression coefficients expressed in terms of bivariate regressions, the multiple regression equation for the value of X, given Y and Z, comes out as:

X = Y(bxy – bxz.bzy)/(1 – byz.bzy) + Z(bxz – bxy.byz)/(1 – bzy.byz).

This is the appropriate equation when X, Y and Z represent deviation values, as assumed here. If we want to use raw values, the partial regression coefficients will be the same, but a non-zero constant must usually be added.

It can be verified by inspection of these formulae that if the independent variables Y and Z are uncorrelated (ryz = byz = bzy = 0), then the partial regression coefficients Bxy.z and Bxz.y reduce to the bivariate regression coefficients bxy and bxz. In this case the multiple regression equation for X given Y and Z therefore reduces to X = bxy.Y + bxz.Z, in which the estimated value of X is the sum of the estimated values given Y and Z separately. This confirms the informal argument given earlier for this special case. (For the other special case, where ryz = 1, the analysis breaks down, as the denominators in the coefficients are zero.)

If there are more than three variables in the analysis, the methods described above can in principle be easily extended. If there are n variables, of which one is chosen as ‘dependent’, we can obtain (n – 1) equations (known as the ‘normal equations’) to determine the (n – 1) partial regression coefficients for the independent variables. These can be expressed in terms of regression or correlation coefficients involving (n – 2) variables, which in turn can be expressed in terms of coefficients of (n – 3) variables, and so on, until coefficients for only 2 variables are reached. The complexity of the resulting formulae rapidly increases with the number of variables, and in practice, before the computer age, multiple regression and correlation were seldom taken beyond four variables. With computers, it is easy to perform multiple regression analysis for any number of variables, but the reliability of the results falls rapidly (due to sampling error and other problems) as the number of variables increases.

On examining the ‘normal equations’ which determine the partial regression coefficients it may also be noted that they are equivalent to equations of the form S(ye) = 0, where y is one of the independent variables and ‘e’ is the ‘error of estimate’ in the value of the dependent variable when the partial regression coefficients are all given their optimum values. But S(ye) = 0 is only true if the correlation between the independent variable and the errors of estimate is zero. This is as it should be, as the errors left over after the best estimate has been made should be random with respect to the variables used in the estimate.

The multiple regression technique essentially solves the ‘problem of prediction’, so far as it can be solved by a linear equation.

**Partial correlation**

The other main problem is how to disentangle the influence and relative importance of each ‘independent’ variable. In this context ‘influence’ does not necessarily imply causal influ  
ence, but often the underlying aim of the analysis is to find out which variables have causal influence on each other. For example, the IQ of parents, their social class, their level of education, and so on, are all likely to be positively correlated, but which of these variables, if any, have an independent influence on the IQ of their children?

Intuitively a plausible approach to this problem is to see what happens if all the independent variables except one are held constant. If there is still a significant correlation between the dependent variable and the remaining independent variable, this cannot be accounted for by any variation in the others (which has been excluded). It is then reasonable to infer that the remaining variable has some independent influence of its own, or at least is correlated with another variable which has such an influence. (The converse inference – that if there is no correlation, then there is no independent influence – is more hazardous, as a true independent influence may have been masked or suppressed by other variables not included in the analysis.)

‘Holding variables constant’ can be done in various ways. Ideally, one would conduct a controlled experiment, with randomisation, control groups, and all the other refinements of experimental technique. But this is not always possible. Where we are forced to rely on existing statistical data, a substitute for experiment is to select for analysis those data for which all the variables except two happen to have the same values. This can be done literally by grouping the data into appropriate sets and calculating correlations or regressions between the two variables of interest when all the other variables have fixed values. But this is laborious, and unless the total sample is very large the resulting correlations and regressions, for each such set of values, are likely to vary from one set to another, even if the underlying relationships are constant. It is usually more convenient to ‘hold variables constant’ by purely statistical methods.

Suppose we have three variables, X, Y, and Z, and we wish to find the correlation or regressions between X and Y while ‘holding Z constant’. For any given value of Z, average values of X and Y can be predicted from the regressions of X and Y on Z. Unless the correlations are perfect, there will be some difference between the observed and the predicted values of X and Y. These differences may be described as the residuals of X and Y given Z. The residuals of X and Y for a given value of Z may be treated as deviations from the mean values of X and Y corresponding to that value of Z. In reality, they are only deviations from the predicted means, and unless the regressions of X and Y on Z are perfectly linear (which they seldom are), some error will introduced. But subject to this qualification, the residuals may be treated as deviation values for the purpose of calculating correlations and regressions between them. The deviation values of X, given Z, can therefore be expressed as X – bxz.Z, where X is the observed value and bxz.Z is the predicted value of X from its regression on Z. Similarly the deviation values of Y, given Z, can be expressed as Y – byz.Z. The standard deviation of the residuals of X, given Z, will be \#(1- rxz^2)sx, that is, the square root of the variance in X remaining after the correlation with Z has ‘explained’ (1- rxz^2) of the original variance. Similarly the standard deviation of the residuals of Y, given Z, will be \#(1- ryz^2)sy.

Using the standard formula for the correlation between two variables, and treating the residuals as the relevant variables, we get a correlation expressed by S(X – bxz.Z)(Y – byz.Z)/N.sx(#(1- rxz^2))sy(#(1- ryz^2)). It can be shown that this is equivalent to (rxy – rxz.ryz)/#(1 – rxz^2)#(1 – ryz^2). \[Note 1\] We may call this Rxy.z, or the partial correlation between X and Y given Z.

By similar methods it can be shown that the coefficient of the regression of the residuals of X on the residuals of Y is equal to (bxy – bxz.bzy)/(1 – byz.bzy). \[Note 2\] It will be seen that this is the same as the partial regression coefficient of X on Y, given Z, which was derived by entirely different methods in solving the ‘problem of prediction’. The two problems therefore turn out to be closely connected.

It would be possible, though cumbersome, to extend the method of residuals to a system of more than three variables. For example, with the four variables W, X, Y, and Z, we could use the multiple regression equations for three variables to estimate separately the values of W and X, given Y and Z, then subtract the estimated values of W and X from their observed values to get the residuals of W and X, given Y and Z, then find the regressions and correlation between the residuals. The coefficients derived in this way should be the same as those derived by the method of least squares for a system of four variables.

The following relationships can also be demonstrated. As this requires some tedious algebra, I will not give full proofs. These relationships are presumably well known to statisticians, but I have not seen them mentioned in most textbooks, so it may be useful to bring them together.

\(a\) Rxy.z = Bxy.z.#(1- rxz^2)sy/#(1- ryz^2)sx. Just as ordinary bivariate correlation coefficients can be converted into regression coefficients, and vice versa, by multiplying them and dividing them by the appropriate standard deviations, so can partial correlation and partial regression coefficients, using standard deviations of residuals.

\(b\) If we take the partial regression coefficient Bxy.z, expressed in terms of the residuals of X and Y, given Z, and divide these residuals by their own standard deviations, the partial regression coefficients are converted into the partial correlation coefficient Rxy.z.

\(c\) After allowing for the regression of the residuals of X on the residuals of Y, the variance of the residuals of X is reduced by (1 – Rxy.z^2), as compared with their original variance.

\(d\) Rxy.z is the mean proportional between the two partial regression coefficients Bxy.z and Byx.z.

These results, taken together, show that the partial regression and correlation between X and Y, given Z, have all the essential properties of bivariate regression and correlation, with the residuals of X and Y, given Z, treated as the correlated variables. This is often described as ‘controlling for Z’, or ‘holding Z constant’, or ‘partialling out Z’. With certain qualifications, it may be said that if we take any particular value of Z, and consider only the values of X and Y corresponding to that value of Z, the regressions and correlation between these values of X and Y will be as expressed by the partial regression and correlation coefficients. For example, if X represents children’s ability at reading, Y represents their ability at arithmetic, and Z represents their IQ, then the partial correlation between X and Y, given Z, should equal the bivariate correlation between ability at reading and arithmetic for children with the same IQ. Real examples are seldom as neat as this account suggests, and the regression and correlation between X and Y for given Z, as calculated directly from the data, are likely to vary somewhat for different values of Z. If it is of practical importance to be sure of the true correlation between X and Y for some particular value of Z, it is desirable to calculate this directly from the data.

Since the partial correlation coefficient is the same as the bivariate correlation between residuals, its value must lie between 1 and -1 (see Part 2). On trying values for the component parts of the partial correlation coefficient in the usual form (rxy – rxz.ryz)/#(1 – rxz^2)(1 – ryz^2), it may be found that some combinations of the components rxy, rxz, and ryz would lead to values outside the range 1 to -1. This shows that some combinations would be inconsistent, and cannot actually arise. This problem, and its  
implications, is discussed in most of the textbooks. A point which I have not seen discussed is that if either of the correlations rxz and ryz is perfect (1 or -1), then the partial correlation coefficient is indeterminate, since the denominator is zero. If we regard the partial correlation as a bivariate correlation between the residuals of X and Y for a fixed value of Z, the correlation will be indeterminate if either of the residuals has no variance, which is the case when rxz or ryz is perfect.

**The dual role of partial regression coefficients**

It should be noted that the partial regression coefficients can be used in two ways. When multiplied by the full deviation of the relevant independent variable, they contribute to the best estimate of the value of the dependent variable as given by the multiple regression equation. When multiplied by the residual deviation of the relevant independent variable, controlling for the other independent variable, they give the best estimate of the residual deviation of the dependent variable.

It may seem surprising that the same coefficient can serve these two different purposes. We can however regard the partial regression coefficient as measuring the expected change in X associated with a unit change in Y, when Z is held constant. It is not unreasonable that the proportionate change (as expressed by the coefficient) might be the same even though the actual size of the change may vary according to whether full or residual deviations are being used.

In any event, it can be proved that the two uses of the partial correlation coefficients are consistent. Suppose we compare the two different estimates resulting from these two uses. To estimate the full deviation of X we have:

(1)…….(estimated) X = Bxy.z.Y + Bxz.y.Z

To estimate the residual deviation of X, based on the value of Y after controlling for Z, we have (estimated) X – bxz.Z = Bxy.z.(Y – byz.Z). But the only estimated quantity in this equation is X (i.e. the full deviation of X), so we can rearrange the equation to give an explicit estimate of X based on the role of the partial regression coefficient in estimating the residual deviation of X. This gives us:

(2)……(estimated) X = Bxy.z(Y – byz.Z) + bxz.Z

Equations (1) and (2) therefore give us two estimates for the full deviation of X based on the two different applications of the partial regression coefficient. These estimates appear at first sight to be different. Notably, equation (2) shows no trace of the partial regression coefficient Bxz.y. I was therefore gratified to find that the right hand sides of the two equations are in fact equivalent. \[Note 3\] So there is no doubt that the two different applications of the partial regression coefficients are consistent, even if it is not intuitively obvious why this is so.

**Beta weights**

For reasons of computational convenience, some authors introduce coefficients known as Beta coefficients or Beta weights. These are not in general the same as either the partial regression or partial correlation coefficients. They can be derived from the partial regression coefficients by dividing each variable by its own (full, not residual) standard deviation. They may therefore be considered in a sense as standardised partial regression coefficients, and it is arguable that the Beta weights provide the best way of evaluating the relative importance of the different independent variables in determining the value of the dependent variable (see further below). The Beta weight for the regression of X on Y given Z can be written as Beta_xy.z. Like the partial correlation coefficient, Beta weights can be expressed in terms of bivariate correlation coefficients. For example, Beta_xy.z is (rxy – rxz.ryz)/(1 – ryz^2). \[Note 4\]

Equivalences between Beta weights, partial correlation coefficients, and partial regression coefficients, can be set out as follows:

Bxy.z =

(bxy – bxz.bzy)/(1 – byz.bzy) =

(rxy.sx/sy – (rxz.sx/sz)(ryz.sz/sy)/\[1 – (ryz.sy/sz)( ryz.sz/sy)\] =

\[(rxy – rxz.ryz)/(1 – ryz^2)\].sx/sy =

Beta_xy.z.(sx/sy) =

Rxy.z.\[sx.#(1 – rxz^2)\]/\[sy.#(1 – ryz^2)\]

and

Beta_xy.z =

Rxy.z..#(1 – rxz^2)\]/#(1 – ryz^2) =

Bxy.z.sy/sx.

It may be noted that if all the standard deviations of X, Y and Z are equal (as would be the case if the standard deviations themselves are the units of measurement, and therefore by definition equal to 1), then the partial regression coefficients are equal to the beta weights.

**Multiple correlation**

We have defined partial regression and correlation, and multiple regression. There is also a multiple correlation. This is a kind of correlation between the dependent variable and the totality of independent variables. In the case of two variables, we can ask how much of the variance in one variable is ‘explained’ by its regression on the other, and similarly in the case of more than two we can ask how much of the variance of the dependent variable is explained by its multiple regression on all the others. For two variables, the correlation explains r^2 of the original variance, so for multiple correlation we may stipulate by definition that the multiple regression explains R^2 of the variance in the dependent variable. (I will assume that the dependent variable is X, so that R^2 is the square of the multiple correlation between X and the independent variables Y and Z.) R can then be interpreted as the multiple correlation coefficient. In practice, R itself is of little interest, so results are usually expressed in terms of R^2. A bewildering variety of formulae are used to express R^2 in terms of bivariate regression or correlation coefficients. One is R^2 = (rxy^2 + rxz^2 – 2rxy.rxz.ryz)/(1 – ryz^2). Another, which superficially looks quite different but can be proved equivalent, is Beta_xy.z.rxy + Beta_xz.y.rxz, where the Betas are as described above.

As in the case of two variables, the variance of the dependent variable can be broken down into two additive components: the variance of the estimates given by the regression and the variance of residuals (the differences between the estimated and observed values). In the case of three variables (one dependent and two independent) the estimate given by the regression is Bxy.z.Y + Bxz.y.Z. Since the mean of the estimates is 0 (assuming that deviation values are used throughout), the variance of the estimates is R^2.VX = \[S(Bxy.zY + Bxz.yZ)^2\]/N. This can be expanded as:

R^2 = (Bxy.z^2.SY^2 + Bxz.y^2.SZ^2 + 2Bxy.z.Bxz.y.SYZ)/NVx

= (Bxy.z^2.NVy + Bxz.y^2.NVz + 2Bxy.z.Bxz.y.Nsy.sz.ryz)/NVx

= Bxy.z^2.Vy/Vx + Bxz.y^2.Vz/Vx + 2Bxy.z.Bxz.y.sy.sz.ryz/Vx

We therefore have yet another expression for the squared multiple correlation coefficient, which can by proved (after some gruesome algebra) to be equivalent to the earlier formulae.

This expression takes a simpler form if all variables have been measured in units of their standard deviation, so that we have sx = sy = sz = Vx = Vy = Vz = 1. R^2 is then simply:

Bxy.z^2 + Bxz.y^2 + 2Bxy.z.Bxz.y.ryz.

Since in this case the Beta weights are equal to the partial regression coefficients, we could substitute Beta’s for the B’s. This formula is particularly important in connection with Sewall Wright’s method of path analysis.

**Problems of interpretation**

As was stated earlier, one of the main aims of multivariate analysis is to disentangle the independent influence of one variable when all other variables are taken into account (‘held constant’). Provided all the relationships are approximately linear, it can be said that if any pair of variables have non-zero partial regression and correlation coefficients between them, then they have some relationship which is not ful  
ly explained by their relationships with the other variables considered. However, neither the partial regression nor partial correlation coefficients are ideal for quantifying the importance of the relationship. In the case of the partial correlation coefficients, a coefficient might be high but still explain little of the total variance in the dependent variable. For example, if X and Y both have a high correlation with Z, the residual variance in both X and Y will be small. The residual variance in Y might then explain most of the residual variance in X, so that the partial correlation coefficient Rxy.z would be high, but it would not be safe to infer that Y is an important influence on X overall. The partial regression coefficients may be more useful for this purpose, but the contribution of each independent variable to the overall variance of the dependent variable still depends not only on the partial regression coefficients but on the variance in each independent variable itself. The best measure of the contribution of each independent variable should therefore take account of its variance as well as the value of the partial regression coefficients.

If we consider the squared multiple correlation coefficient in the form Bxy.z^2.Vy/Vx + Bxz.y^2.Vz/Vx + 2Bxy.z.Bxz.y.sy.sz.ryz/Vx, it will be seen that the independent variables Y and Z separately account for Bxy.z^2.Vy/Vx and Bxz.y^2.Vz/Vx of the total variance. But these quantities equal the squares of the Beta weights for these variables. The Beta weights (or their squares) therefore appear to give the best indication of the relative importance of the independent variables. It will however also be seen that the third term 2Bxy.z.Bxz.y.sy.sz.ryz/Vx, which involves the correlation ryz between the independent variables, also contributes to the variance. If the correlation is high, this term may well account for much of the total. The independent variables considered separately therefore do not give the whole picture. If they are positively correlated the variance of the estimates will be greater than otherwise, as there will be more relatively high or low estimates than if they were combined by chance. (If they are negatively correlated the reverse will be the case.) These joint contributions due to the correlation of independent variables cannot properly be allocated to the variables separately.

Multivariate correlation and regression raise some paradoxes and difficulties of interpretation which do not arise with the simpler bivariate case. These are discussed more or less adequately in the textbooks. For example, the accuracy of estimation can often be increased by taking account of a variable which is not itself correlated with the dependent variable. Suppose the dependent variable is X and we have correlations rxy = .4, rxz = 0, and ryz = .7. Here the independent variable Y explains only .16 (i.e. .4^2) of the variance in X, while the independent variable Z, being uncorrelated with X, explains none of its variance. But if we take the squared multiple correlation coefficient in the form (rxy^2 + rxz^2 – 2rxy.rxz.ryz)/(1 – ryz^2), for the given values this equals (.16 + 0 – 0)/.51 = .31. The accuracy of the estimation of X is therefore nearly doubled as compared with the estimate based on the correlations rxy and rxz alone. This seems counterintuitive, as the correlation between Y and Z appears to give us no new information about X. The puzzle can be partly resolved by noting that the combination of all three correlations does give us new information about X, as it implies that the partial correlation between X and Y, for given Z, is negative, which we would not know from rxy and rxz alone.

From the expression for the partial correlation coefficient, Rxy.z = (rxy – rxz.ryz)/\[#(1 – rxz^2)(1 – ryz^2)\], it is evident that if rxy = rxz.ryz, then the partial correlation coefficient is zero. The product rxz.ryz may therefore be interpreted as the expected level of rxy if the correlation between X and Y is due solely to their correlations with Z. If rxz.ryz is less than rxy, then the partial correlation coefficient is positive, whereas if rxz.ryz is greater than rxy, the partial correlation coefficient is negative. In particular, if X and Y are uncorrelated with each other, but both are positively correlated with Z, then the partial correlation coefficient between X and Y must be negative. Some authors have found this paradoxical, and a reason for dissatisfaction with multivariate analysis.

I am not sure that there is any real paradox here. Suppose for example that X and Y are uncorrelated variables measured in the same units (e.g. weight), while Z is a third variable formed by adding together the values of corresponding elements from each of X and Y. Z will therefore be positively, but not perfectly, correlated with both X and Y. What then will be the partial correlation between X and Y, given Z? A little consideration should show that it will be negative. It is important to note that the partial correlation between X and Y, holding Z constant, depends on the covariance between the deviation values of X and Y at a given level of Z. The deviation values of X and Y must therefore be measured relative to the average values of X and Y for that level of Z. Suppose we consider the set of all those Z items which have the value A. For each item, A is by assumption the sum of the values of the associated X and Y items. If the mean value of the associated X items, for Z = A, is B, and that of the associated Y items is C, it is easy to see that A = B + C, since SZ = SX + SY, and we need only divide through by the number of items to get A = B + C. For any particular X item, its value will usually be greater or less than B (the mean value of the relevant X items) by some (varying) amount D, but in this case the value of the associated Y item must be less or greater than C (the mean value of the relevant Y items) by an equal and opposite amount D, since their total must be A = B + C = (B + D) + (C – D), or (B – D) + (C + D). The deviations of the associated X and Y values from their own means will therefore be of opposite signs (unless by chance they are both zero). The covariance of the X and Y values, for a given value of Z, will be negative, and as a result the partial correlation between X and Y will also be negative. This is of course a simplified example, but relationships of this general kind are probably quite common, and should not be regarded as paradoxical.

As in the bivariate case, the standard treatment of multivariate regression assumes that the best estimate of the dependent variable, given the value of the independent variables, can be expressed by a linear equation. If the true relationships of the variables are significantly non-linear, the multiple regression will explain less of the variance than would be possible using non-linear regressions. It is still ‘better than nothing’, but the individual partial regression and correlation coefficients may be severely distorted, and may conceivably be changed from positive to negative, or vice versa, if the true relationships are non-linear. It is therefore unsafe to draw conclusions about the relative importance of different variables from a linear regression analysis if the true relationships are non-linear. Since this is one of the main purposes for which multivariate regression is used, this is a severe drawback.

A final problem to note is that the practical validity of multiple regression and correlation analysis depends on the identification of all relevant explanatory variables. If there is an important variable left out of the analysis (a so-called ‘lurking variable’), the inclusion of that variable might seriously change the results of the original analysis.

Note 1: We start with the formula for the correlation between the residuals of X on the residuals of Y:

S(X – bxz.Z)(Y – byz.Z)/N.sx(#(1- rxz^2))sy(#(1- ryz^2)).

The numerator can be expanded as SXY – SYZ.bxz  
– SXZ.byz + SZ^2.bxz.byz.

Noting the equivalences SXY = rxy.Nsx.sy, SYZ = ryz.Nsy.sz, SXZ = rxz.Nsx.sz, bxz = rxz.sx.sz/Vz, byz = ryz.sy.sz/Vz, and SZ^2 = NVz, the numerator can be reformulated as:

rxy.N.sx.sy – ryz.Nsy.sz.rxz.sx.sz/VZ – rxz.Nsx.sz.ryz.sy.sz/Vz + NVz.(rxz.sx.sz/Vz)(ryz.sy.sz/Vz)

which can be simplified to

rxy.N.sx.sy – rxz.ryz.N.sx.sy.

But the denominator N.sx(#(1- rxz^2))sy(#(1- ryz^2)) also contains the factor N.sx.sy, so cancelling this from numerator and denominator we get

(rxy – rxz.ryz)/#(1- rxz^2)#(1- ryz^2)

as required.

Note 2: We start with the formula for the regression of the residuals of X on the residuals of Y:

S(X – bxz.Z)(Y – byz.Z)/NVy(1- ryz^2)

The numerator can be expanded as:

SXY – SYZ.bxz – SXZ.byz + SZ^2.bxz.byz

Noting the equivalences SXY = bxy.NVy = byx.NVx, SYZ = byz.NVz = bzy.NVy, SXZ = bxz.NVz = bzx.NVx, and SZ^2 = NVz, this can be reformulated as:

bxy.NVy – bzy.NVy.bxz – bxz.NVz.bzy.NVy/NVz + NVz.bxz.bzy.NVy/NVz =

(bxy – bxz.bzy)NVy

But the denominator also contains the factor NVy, so cancelling this from numerator and denominator we get the following formula for the regression of the residuals of X on the residuals of Y:

(bxy – bxz.bzy)/(1- ryz^2) =

(bxy – bxz.bzy)/(1 – byz.bzy).

But this is the same as Bxy.z, the partial regression coefficient of X on Y, given Z.

Note 3: We wish to prove that Bxy.z(Y – byz.Z) + bxz.Z = Bxy.zY + Bxz.y.Z.

Expressing Bxy.z in terms of bivariate regression coefficients, we have for the left-hand-side \[(bxy – bxz.bzy)/(1 – byz.bzy)\]Y – byz\[(bxy – bxz.bzy)/(1 – byz.bzy)\]Z + bxz.Z.

Collecting together the coefficients of Z and expressing them with the common denominator (1 – byz.bzy), we have for the Z term  
\[\[bxz.(1 – byz.bzy) – byz.(bxy – bxz.bzy)\]/(1 – byz.bzy)\]Z.

But the coefficient of Z simplifies to (bxz – byz.bxy)/(1 – byz.bzy), so we have for the left-hand-side as a whole \[(bxy – bxz.bzy)/(1 – byz.bzy)\]Y + \[(bxz – byz.bxy)/(1 – byz.bzy)\]Z.

On inspection this can be seen to be equivalent to Bxy.z.Y + Bxz.y.Z, which is what we wished to prove.

Note 4: We require to prove that if the variables in the partial regression coefficient Bxy.z are divided by their own standard deviations, the result can be expressed in the form (rxy – rxz.ryz)/(1 – ryz^2).

Consider the partial regression coefficient Bxy.z in the form \[Sxy/NVy – (Sxz/NVz)(Szy/NVy)\]/\[1 – Syz.Szy/NVz.NVy\]. We now divide each variable by its own standard deviation. Here we note that the variance Vx is an abbreviation for S(x^2)/N (using deviation values). If the X variable is divided by its standard deviation, the variance of the resulting transformed variables is S(X/sx)^2)/N = (Sx^2)/NVx = 1. Likewise for the other variances. Dividing all the variables by their standard deviations, \[Sxy/NVy – (Sxz/NVz)(Szy/NVy)\]/\[1 – Syz.Szy/NVzNVy\] therefore reduces to \[Sxy/Nsx.sy – (Sxz/Nsx.sz)(Szy/Nsz.sy)\]/\[1 – (Syz/Nsy.sz)(Szy/Nsz.sy)\]. On inspection this is equivalent to (rxy – rxz.ryz)/(1 – ryz^2), which is the required expression for Beta_xy.z. Proving the remaining equivalences is tedious but relatively straightforward.

### Related Posts:

- [Correlation in the hiz
  house](https://www.gnxp.com/WordPress/2007/09/07/correlation-in-the-hiz-house/) - [Sewall Wright & the Shifting Balance Theory (part
  II)](https://www.gnxp.com/WordPress/2008/11/09/sewall-wright-the-shifting-balance-theory-part-ii/) - [Notes on Correlation: Part
  2](https://www.gnxp.com/WordPress/2007/11/19/notes-on-correlation-part-2/) - [Notes on Sewall Wright: Path
  Analysis](https://www.gnxp.com/WordPress/2008/03/15/notes-on-sewall-wright-path-analysis/) - [Correlation structure of
  traits](https://www.gnxp.com/WordPress/2007/09/21/correlation-structure-of-traits/) - [Wright, Fisher, Haldane, and odds and
  ends](https://www.gnxp.com/WordPress/2008/11/27/wright-fisher-haldane-and-odds-and-ends/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F01%2F24%2Fnotes-on-correlation-part-3%2F&linkname=Notes%20on%20Correlation%3A%20%20Part%203 "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F01%2F24%2Fnotes-on-correlation-part-3%2F&linkname=Notes%20on%20Correlation%3A%20%20Part%203 "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F01%2F24%2Fnotes-on-correlation-part-3%2F&linkname=Notes%20on%20Correlation%3A%20%20Part%203 "Email")[](https://www.addtoany.com/share)
