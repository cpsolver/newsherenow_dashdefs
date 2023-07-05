This open-source Dashrep code implements the web API at NewsHereNow.com, which is documented at <a href="http://www.newsherenow.com/web_api.html">NewsHereNow.com/web_api.html</a>.
====================


Software license
----------------

(c) Copyright 2023 by Fovationz, Inc. at NewsHereNow.com .  Currently all rights are reserved.  Future changes in this license are likely.
Disclaimer of Warranty:  THERE IS NO WARRANTY FOR THIS SOFTWARE. THE COPYRIGHT HOLDER PROVIDES THE SOFTWARE "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE FITNESS FOR A PARTICULAR PURPOSE.  Limitation of Liability:  IN NO EVENT WILL THE COPYRIGHT HOLDER BE LIABLE TO ANYONE FOR DAMAGES, INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING OUT OF THE USE OR INABILITY TO USE THE SOFTWARE.


Overview
--------

Use of this software is documented at: <a href="http://www.newsherenow.com/web_api.html">NewsHereNow.com/web_api.html</a>

This code is written in the Dashrep programming language, which is documented at <a href="http://www.dashrep.org">Dashrep.org</a>.  That webpage points to the location of the Dashrep compiler.


Latitude and longitude format
-------------

For faster processing, latitudes and longitudes are converted into, and then handled as, positive integers, without a decimal point and without any minus sign.  To convert any such integer back into a signed decimal number, if the first digit is <i>1</i> then remove the <i>1</i> and insert a decimal point to the left of the right-most eight digits, or else if the first digit is <i>0</i> then add a minus sign and convert each digit to its "nines complement" value.  The "nines complement" conversion changes each <i>9</i> to <i>0</i>, each <i>8</i> to <i>1</i>, each <i>7</i> to <i>2</i>, etc. down to each <i>2</i> to <i>7</i>, each <i>1</i> to <i>8</i>, and each <i>0</i> to <i>9</i>.  Using this convention causes the numbers to have smooth transitions at the equator (10000000000) and zero meridian (10000000000).  Specifically the next point in the negative direction is <i>09999999999</i>.  Note that these conversions are text-based so they do not involve converting to or from software-based "integers".


History
=======

This software was written by Richard Fobes.
