+++
title = "Meat for your money"
full_title = "Meat for your money"
date = "2009-09-22"
upstream_url = "https://www.gnxp.com/WordPress/2009/09/22/meat-for-your-money/"

+++
Source: [here](https://www.gnxp.com/WordPress/2009/09/22/meat-for-your-money/).

Meat for your money

I stumbled onto [these data](https://spreadsheets.google.com/ccc?key=tQqrHfPbFdL7npbGzWW0nsQ) which show meat consumption in kilograms over the years for a range of nations. I was curious as to the relationship between meat consumption & GDP PPP per capita. My logic is that the more \$ you have the more calories you’ll purchase in form of flesh protein & fat. That being said, there’s obviously a limit to how many calories you might want to purchase per day, so extra cost of meat for the wealthy would be in the form of quality (e.g., eating only Kobe beef). I took the 2002 data on meat consumption and plotted it against GDP PPP per capita from 2007. The relationship is rather straightforward.

The thick black line is a fit via [loess](https://en.wikipedia.org/wiki/Local_regression). Here’s a plot that’s log-transformed:

OK, but what you want to do are the **deviations from the trend line, right?** If you’re “Green” minded, the “naughty and the nice.”

|                        |                         |                              |                                    |               |                            |
|------------------------|------------------------:|-----------------------------:|-----------------------------------:|--------------:|---------------------------:|
| **Country**            | **GDP per capita 2007** | **kg meat consumed in 2002** | **kg meat consumed** **predicted** | **Deviation** | **Proportional Deviation** |
|                        |                         |                              |                                    |               |                            |
| Mongolia               |                 \$2,894 |                        108.8 |                              22.75 |         86.05 |                       478% |
| Papua New Guinea       |                 \$2,079 |                           73 |                              18.76 |         54.24 |                       389% |
| Samoa                  |                 \$4,802 |                         82.6 |                              31.12 |         51.48 |                       265% |
| Paraguay               |                 \$4,004 |                         70.3 |                              27.78 |         42.52 |                       253% |
| Kyrgyzstan             |                 \$1,997 |                           39 |                              18.34 |         20.66 |                       213% |
| Uruguay                |                \$10,836 |                         98.6 |                              47.64 |         50.96 |                       207% |
| Grenada                |                \$12,315 |                           97 |                              50.87 |         46.13 |                       191% |
| Argentina              |                \$13,061 |                         97.6 |                              52.91 |         44.69 |                       184% |
| Brazil                 |                 \$9,731 |                         82.4 |                              45.66 |         36.74 |                       180% |
| Zimbabwe               |                   \$190 |                         15.2 |                               8.46 |          6.74 |                       180% |
| Belize                 |                 \$8,302 |                         74.7 |                               42.6 |          32.1 |                       175% |
| Mauritania             |                 \$1,827 |                         29.9 |                              17.48 |         12.42 |                       171% |
| Bolivia                |                 \$4,359 |                           50 |                               29.3 |          20.7 |                       171% |
| French Polynesia       |                \$18,421 |                        112.2 |                               68.1 |          44.1 |                       165% |
| New Zealand            |                \$27,310 |                        142.1 |                               86.8 |          55.3 |                       164% |
| China                  |                 \$5,371 |                         52.4 |                              33.32 |         19.08 |                       157% |
| Denmark                |                \$37,179 |                        145.9 |                              93.21 |         52.69 |                       157% |
| Dominica               |                 \$8,952 |                         67.1 |                              44.13 |         22.97 |                       152% |
| Cyprus                 |                \$27,142 |                        131.3 |                              86.57 |         44.73 |                       152% |
| Saint Kitts and Nevis  |                \$18,323 |                         99.3 |                              67.82 |         31.48 |                       146% |
| Hungary                |                \$19,255 |                        100.7 |                              70.45 |         30.25 |                       143% |
| Jamaica                |                 \$7,367 |                         56.8 |                              39.93 |         16.87 |                       142% |
| Bulgaria               |                \$11,841 |                         69.4 |                              49.69 |         19.71 |                       140% |
| New Caledonia          |                \$13,990 |                         76.6 |                              55.48 |         21.12 |                       138% |
| Madagascar             |                   \$948 |                         17.6 |                              12.79 |          4.81 |                       138% |
| Mali                   |                 \$1,136 |                           19 |                              13.82 |          5.18 |                       137% |
| Lebanon                |                \$10,302 |                         63.1 |                              46.68 |         16.42 |                       135% |
| Luxembourg             |                \$79,422 |                        141.7 |                             105.43 |         36.27 |                       134% |
| Vietnam                |                 \$2,593 |                         28.6 |                              21.31 |          7.29 |                       134% |
| United States          |                \$45,759 |                        124.8 |                              95.38 |         29.42 |                       131% |
| Spain                  |                \$33,648 |                        118.6 |                              92.14 |         26.46 |                       129% |
| Barbados               |                \$18,900 |                         88.7 |                              69.47 |         19.23 |                       128% |
| Poland                 |                \$16,177 |                         78.1 |                              61.65 |         16.45 |                       127% |
| Philippines            |                 \$3,295 |                         31.1 |                              24.62 |          6.48 |                       126% |
| Belarus                |                \$10,643 |                         58.6 |                              47.29 |         11.31 |                       124% |
| Netherlands Antilles   |                \$15,481 |                         73.3 |                              59.67 |         13.63 |                       123% |
| Guinea-Bissau          |                   \$561 |                           13 |                              10.61 |          2.39 |                       123% |
| Guyana                 |                 \$3,665 |                         31.8 |                               26.3 |           5.5 |                       121% |
| Portugal               |                \$21,827 |                         91.1 |                               76.9 |          14.2 |                       118% |
| Chile                  |                \$14,296 |                         66.4 |                              56.33 |         10.07 |                       118% |
| Canada                 |                \$38,065 |                        108.1 |                              93.46 |         14.64 |                       116% |
| Fiji                   |                 \$5,529 |                         39.1 |                               33.9 |           5.2 |                       115% |
| Panama                 |                \$10,737 |                         54.5 |                              47.46 |          7.04 |                       115% |
| Mexico                 |                \$12,447 |                         58.6 |                              51.23 |          7.37 |                       114% |
| Ecuador                |                 \$7,176 |                           45 |                              39.35 |          5.65 |                       114% |
| Vanuatu                |                 \$4,232 |                         32.6 |                              28.76 |          3.84 |                       113% |
| Romania                |                \$11,093 |                         54.5 |                              48.13 |          6.37 |                       113% |
| Sudan                  |                 \$2,056 |                           21 |                              18.65 |          2.35 |                       113% |
| France                 |                \$31,161 |                        101.1 |                              90.79 |         10.31 |                       111% |
| Ireland                |                \$46,628 |                        106.3 |                              95.58 |         10.72 |                       111% |
| Swaziland              |                 \$4,734 |                         34.2 |                              30.85 |          3.35 |                       111% |
| Albania                |                 \$5,796 |                         38.2 |                              34.86 |          3.34 |                       110% |
| Israel                 |                \$28,911 |                         97.1 |                              88.75 |          8.35 |                       109% |
| Malta                  |                \$23,390 |                         86.9 |                              80.25 |          6.65 |                       108% |
| Venezuela              |                \$12,846 |                         56.6 |                              52.32 |          4.28 |                       108% |
| Senegal                |                 \$1,679 |                         17.7 |                              16.71 |          0.99 |                       106% |
| Namibia                |                 \$5,202 |                           34 |                              32.69 |          1.31 |                       104% |
| Haiti                  |                 \$1,307 |                         15.3 |                              14.75 |          0.55 |                       104% |
| Uzbekistan             |                 \$2,318 |                         20.7 |                              19.96 |          0.74 |                       104% |
| Benin                  |                 \$1,485 |                         16.2 |                               15.7 |           0.5 |                       103% |
| Slovenia               |                \$27,966 |                           88 |                              87.65 |          0.35 |                       100% |
| Austria                |                \$39,269 |                         94.1 |                              93.79 |          0.31 |                       100% |
| Italy                  |                \$30,956 |                         90.4 |                              90.64 |         -0.24 |                       100% |
| Lesotho                |                 \$1,441 |                         15.4 |                              15.46 |         -0.06 |                       100% |
| Niger                  |                   \$687 |                         11.2 |                              11.33 |         -0.13 |                        99% |
| Cape Verde             |                 \$3,784 |                         26.3 |                              26.82 |         -0.52 |                        98% |
| Jordan                 |                 \$4,700 |                         29.8 |                              30.71 |         -0.91 |                        97% |
| Netherlands            |                \$38,955 |                         89.3 |                              93.71 |         -4.41 |                        95% |
| Kazakhstan             |                \$11,004 |                         44.8 |                              47.96 |         -3.16 |                        93% |
| Belgium                |                \$36,229 |                         86.1 |                              92.94 |         -6.84 |                        93% |
| Slovakia               |                \$20,229 |                         67.4 |                              73.03 |         -5.63 |                        92% |
| Guam                   |                \$14,738 |                         52.6 |                              57.57 |         -4.97 |                        91% |
| Uganda                 |                   \$963 |                         11.7 |                              12.87 |         -1.17 |                        91% |
| Iceland                |                \$40,373 |                         84.8 |                              94.08 |         -9.28 |                        90% |
| Chad                   |                 \$1,544 |                         14.3 |                                 16 |          -1.7 |                        89% |
| Malaysia               |                \$14,552 |                         50.9 |                              57.05 |         -6.15 |                        89% |
| Germany                |                \$34,065 |                         82.1 |                              92.28 |        -10.18 |                        89% |
| Russia                 |                \$14,833 |                           51 |                              57.84 |         -6.84 |                        88% |
| Georgia                |                 \$4,434 |                           26 |                              29.61 |         -3.61 |                        88% |
| Estonia                |                \$21,802 |                         67.4 |                              76.84 |         -9.44 |                        88% |
| Greece                 |                \$30,599 |                         78.7 |                              90.36 |        -11.66 |                        87% |
| Kenya                  |                 \$1,658 |                         14.3 |                               16.6 |          -2.3 |                        86% |
| Qatar                  |                \$78,723 |                         90.5 |                             105.09 |        -14.59 |                        86% |
| United Kingdom         |                \$35,047 |                         79.6 |                              92.58 |        -12.98 |                        86% |
| Honduras               |                 \$4,311 |                         24.7 |                              29.09 |         -4.39 |                        85% |
| Colombia               |                 \$7,384 |                         33.9 |                              39.98 |         -6.08 |                        85% |
| Peru                   |                 \$7,658 |                         34.5 |                              40.79 |         -6.29 |                        85% |
| Costa Rica             |                \$11,072 |                         40.4 |                              48.09 |         -7.69 |                        84% |
| Croatia                |                \$15,487 |                         49.9 |                              59.69 |         -9.79 |                        84% |
| Ukraine                |                 \$7,015 |                         32.3 |                              38.86 |         -6.56 |                        83% |
| Gabon                  |                \$14,049 |                           46 |                              55.65 |         -9.65 |                        83% |
| South Africa           |                \$10,632 |                           39 |                              47.27 |         -8.27 |                        82% |
| Sweden                 |                \$37,482 |                         76.1 |                               93.3 |         -17.2 |                        82% |
| Seychelles             |                \$16,826 |                         51.1 |                               63.5 |         -12.4 |                        80% |
| United Arab Emirates   |                \$36,994 |                         74.4 |                              93.16 |        -18.76 |                        80% |
| Armenia                |                 \$5,778 |                         27.7 |                               34.8 |          -7.1 |                        80% |
| Burkina Faso           |                 \$1,215 |                         11.2 |                              14.25 |         -3.05 |                        79% |
| Cambodia               |                 \$1,871 |                         13.9 |                               17.7 |          -3.8 |                        79% |
| Lithuania              |                \$16,776 |                         49.5 |                              63.36 |        -13.86 |                        78% |
| Liberia                |                   \$477 |                          7.9 |                              10.13 |         -2.23 |                        78% |
| Zambia                 |                 \$1,403 |                         11.9 |                              15.26 |         -3.36 |                        78% |
| Morocco                |                 \$3,703 |                         20.6 |                              26.46 |         -5.86 |                        78% |
| Switzerland            |                \$40,134 |                         72.9 |                              94.02 |        -21.12 |                        78% |
| Bahrain                |                \$33,885 |                         70.7 |                              92.22 |        -21.52 |                        77% |
| Nepal                  |                 \$1,013 |                           10 |                              13.15 |         -3.15 |                        76% |
| Singapore              |                \$49,879 |                         71.1 |                              96.31 |        -25.21 |                        74% |
| Cameroon               |                 \$2,228 |                         14.4 |                              19.51 |         -5.11 |                        74% |
| Guatemala              |                 \$5,088 |                         23.8 |                              32.25 |         -8.45 |                        74% |
| Finland                |                \$35,965 |                         67.4 |                              92.86 |        -25.46 |                        73% |
| Antigua and Barbuda    |                \$21,963 |                           56 |                              77.21 |        -21.21 |                        73% |
| Oman                   |                \$18,999 |                         49.8 |                              69.74 |        -19.94 |                        71% |
| Egypt                  |                 \$5,046 |                         22.5 |                              32.09 |         -9.59 |                        70% |
| Yemen                  |                 \$2,530 |                         14.7 |                                 21 |          -6.3 |                        70% |
| Syria                  |                 \$4,679 |                         21.2 |                              30.62 |         -9.42 |                        69% |
| Latvia                 |                \$17,723 |                         45.7 |                              66.08 |        -20.38 |                        69% |
| Trinidad and Tobago    |                \$25,355 |                         57.8 |                              83.86 |        -26.06 |                        69% |
| Togo                   |                   \$884 |                          8.5 |                              12.43 |         -3.93 |                        68% |
| Ethiopia               |                   \$733 |                          7.9 |                              11.58 |         -3.68 |                        68% |
| Tanzania               |                 \$1,297 |                           10 |                              14.69 |         -4.69 |                        68% |
| Cuba                   |                \$11,015 |                         32.2 |                              47.98 |        -15.78 |                        67% |
| Djibouti               |                 \$3,501 |                         17.1 |                              25.56 |         -8.46 |                        67% |
| Thailand               |                 \$8,015 |                         27.9 |                              41.82 |        -13.92 |                        67% |
| Nicaragua              |                 \$2,849 |                         14.9 |                              22.54 |         -7.64 |                        66% |
| Ghana                  |                 \$1,358 |                          9.9 |                              15.02 |         -5.12 |                        66% |
| Tunisia                |                 \$7,403 |                         25.5 |                              40.04 |        -14.54 |                        64% |
| Norway                 |                \$53,285 |                         61.7 |                              97.06 |        -35.36 |                        64% |
| Saudi Arabia           |                \$19,782 |                         44.6 |                              71.87 |        -27.27 |                        62% |
| Kuwait                 |                \$55,876 |                         60.2 |                              97.64 |        -37.44 |                        62% |
| El Salvador            |                 \$5,992 |                         21.4 |                              35.54 |        -14.14 |                        60% |
| Bosnia and Herzegovina |                 \$6,085 |                         21.4 |                              35.86 |        -14.46 |                        60% |
| Pakistan               |                 \$2,500 |                         12.3 |                              20.85 |         -8.55 |                        59% |
| Brunei                 |                \$52,432 |                         56.4 |                              96.87 |        -40.47 |                        58% |
| Maldives               |                 \$4,303 |                         16.6 |                              29.06 |        -12.46 |                        57% |
| American Samoa         |                 \$8,949 |                         24.9 |                              44.12 |        -19.22 |                        56% |
| Libya                  |                \$12,377 |                         28.6 |                              51.04 |        -22.44 |                        56% |
| Sierra Leone           |                   \$650 |                          6.1 |                              11.11 |         -5.01 |                        55% |
| Tajikistan             |                 \$1,690 |                          8.7 |                              16.77 |         -8.07 |                        52% |
| Algeria                |                 \$6,669 |                         18.3 |                              37.78 |        -19.48 |                        48% |
| Botswana               |                \$14,343 |                         27.3 |                              56.47 |        -29.17 |                        48% |
| Guinea                 |                 \$1,102 |                          6.5 |                              13.63 |         -7.13 |                        48% |
| Japan                  |                \$33,523 |                         43.9 |                              92.09 |        -48.19 |                        48% |
| Iran                   |                \$11,666 |                         23.1 |                               49.3 |         -26.2 |                        47% |
| Angola                 |                 \$7,784 |                           19 |                              41.16 |        -22.16 |                        46% |
| Mozambique             |                   \$844 |                          5.6 |                              12.21 |         -6.61 |                        46% |
| Nigeria                |                 \$2,193 |                          8.6 |                              19.33 |        -10.73 |                        44% |
| Comoros                |                 \$1,774 |                          7.6 |                               17.2 |          -9.6 |                        44% |
| Malawi                 |                   \$778 |                          5.1 |                              11.84 |         -6.74 |                        43% |
| Turkey                 |                \$12,000 |                         19.3 |                              50.07 |        -30.77 |                        39% |
| Azerbaijan             |                 \$7,963 |                         15.9 |                              41.68 |        -25.78 |                        38% |
| Burundi                |                   \$346 |                          3.5 |                               9.37 |         -5.87 |                        37% |
| Rwanda                 |                   \$813 |                          4.4 |                              12.04 |         -7.64 |                        37% |
| Indonesia              |                 \$3,595 |                          8.3 |                              25.98 |        -17.68 |                        32% |
| French Guiana          |                 \$8,298 |                         13.2 |                              42.59 |        -29.39 |                        31% |
| Guadeloupe             |                 \$7,981 |                         12.7 |                              41.73 |        -29.03 |                        30% |
| Martinique             |                \$14,360 |                         13.9 |                              56.52 |        -42.62 |                        25% |
| India                  |                 \$2,625 |                          5.2 |                              21.46 |        -16.26 |                        24% |
| Sri Lanka              |                 \$3,919 |                          6.6 |                              27.42 |        -20.82 |                        24% |
| Bangladesh             |                 \$1,385 |                          3.1 |                              15.16 |        -12.06 |                        20% |
| Bhutan                 |                 \$1,443 |                            3 |                              15.47 |        -12.47 |                        19% |
| Virgin Islands         |                \$14,498 |                          6.6 |                               56.9 |         -50.3 |                        12% |

The Virgin Islands is entered like that in the data, so perhaps it is a data entry error….

### Related Posts:

- [The rise of real meat
  factories](https://www.gnxp.com/WordPress/2011/05/25/the-rise-of-real-meat-factories/) - [Meat is
  Great](https://www.gnxp.com/WordPress/2005/02/22/meat-is-great/) - [Ass-kicking is
  stochastic](https://www.gnxp.com/WordPress/2006/11/24/ass-kicking-is-stochastic/) - [No more "observational
  studies"!!!!](https://www.gnxp.com/WordPress/2017/05/15/no-more-observational-studies/) - [Maybe it's agriculture - skin color
  edition....](https://www.gnxp.com/WordPress/2007/10/02/maybe-its-agriculture-skin-color-edition/) - [My new blog about health, nutrition, and
  diet](https://www.gnxp.com/WordPress/2009/06/30/my-new-blog-about-health-nutrition-and-diet/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F09%2F22%2Fmeat-for-your-money%2F&linkname=Meat%20for%20your%20money "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F09%2F22%2Fmeat-for-your-money%2F&linkname=Meat%20for%20your%20money "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2009%2F09%2F22%2Fmeat-for-your-money%2F&linkname=Meat%20for%20your%20money "Email")[](https://www.addtoany.com/share)
