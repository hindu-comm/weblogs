+++
title = "NBCCOM uses PHP?"
full_title = "NBCCOM uses PHP?"
date = "2008-10-05"
upstream_url = "https://www.gnxp.com/WordPress/2008/10/05/nbc-com-uses-php/"

+++
Source: [here](https://www.gnxp.com/WordPress/2008/10/05/nbc-com-uses-php/).

NBC.COM uses PHP?

I was checking out videos on NBC’s Saturday Night Live website, and I got this error:

> Fatal error: Uncaught exception ‘Zend_Db_Adapter_Exception’ with > message ‘SQLSTATE\[08004\] \[1040\] Too many connections’ in > /var/www/common/classes/Zend/Db/Adapter/Pdo/Abstract.php:131 Stack > trace: \#0 /var/www/common/classes/Zend/Db/Adapter/Abstract.php(271): > Zend_Db_Adapter_Pdo_Abstract-\>\_connect() \#1 > /var/www/common/classes/Nbcu/Asset.php(15): > Zend_Db_Adapter_Abstract-\>getConnection() \#2 > /var/www/common/classes/Nbcu/Controller/Scet/Video.php(11): > Nbcu_Asset-\>\_\_construct() \#3 /var/www/www.nbc.com/htdocs/app/bootstrap/scet/video.php(10): Nbcu_Controller_Scet_Video-\>dispatch() \#4 {main} thrown in /var/www/common/classes/Zend/Db/Adapter/Pdo/Abstract.php on line 131

I’m a little surprised that such a high traffic corporate site is running with [PHP](https://en.wikipedia.org/wiki/PHP). Not too surprised about the crappy exception handling though…when higher ups are breathing down your neck handling these sorts of breakdowns often gets pushed to the bottom of the task stack. But with PHP’s history of security problems I would think not exposing errors like this is even more important.

### Related Posts:

- [Battery not
  charging....](https://www.gnxp.com/WordPress/2007/10/26/battery-not-charging/) - [Question for the hardware
  geeks](https://www.gnxp.com/WordPress/2006/05/11/question-for-the-hardware-geeks/) - [Around
  ScienceBlogs](https://www.gnxp.com/WordPress/2009/06/17/around-scienceblogs-8/) - [Personal genomics &
  NEJM](https://www.gnxp.com/WordPress/2009/04/15/personal-genomics-amp-nejm/) - [Andy Samberg + Mahmoud Ahmadinejad → MSM
  (?)](https://www.gnxp.com/WordPress/2007/10/01/andy-samberg-mahmoud-ahmadinejad-rarr-msm/) - [We are our sister's
  keeper....](https://www.gnxp.com/WordPress/2009/02/06/we-are-our-sisters-keeper/)

### *Related*

[](https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F10%2F05%2Fnbc-com-uses-php%2F&linkname=NBC.COM%20uses%20PHP%3F "Facebook")[](https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F10%2F05%2Fnbc-com-uses-php%2F&linkname=NBC.COM%20uses%20PHP%3F "Twitter")[](https://www.addtoany.com/add_to/email?linkurl=https%3A%2F%2Fwww.gnxp.com%2FWordPress%2F2008%2F10%2F05%2Fnbc-com-uses-php%2F&linkname=NBC.COM%20uses%20PHP%3F "Email")[](https://www.addtoany.com/share)
