###**Customizable Streamhub Map ReadMe**


-----
This app expands on the Streamhub Map application by allowing the user to easily customize the collection displayed by the Streamhub map and certain displays options through the url.


---

####Parameter Definitions

**n=example.com:**  The network of the collection to be displayed.  This is one of the customizable parameters and not necessarily the base url.

**s=x:** Sets the Site ID of the collection to be displayed.

**a=y:** Sets the article ID of the collection to be displayed.

These three variables are used to select which collection you want to display on the map

(Information for finding variables for the first three parameters can be found on the livefyre admin console - instructions below)

**e=anotherexample.com:** Sets the environment for the collection to be displayed (defaults to livefyre.com. - this is not shown in the example urls below since it does not need to be altered or customized to work under normal circumstances.)

**c=a,b:** Sets the map's starting center at latitude 'a' and longitude 'b.'   Decimal values are allowed here.

 Positive latitude values correspond to North and negative values correspond to South, positive longitude correspond to East, negative to West (for example entering 42, 122 would make the map's initial center 42 degrees North, 122 degrees East while -42, -122 sets the initial location to 42 degrees South, 122 Degrees West.)

 (Note: The comma between latitude and longitude values IS REQUIRED FOR THIS TO WORK.  Also there should be no spaces between the values - inserting spaces can and will cause errors.) 

**z=x:** Sets the starting zoom level to x - this parameter takes whole numbers from 0 to 18 - 4 is the default and 3 is the minimum recommended zoom. 

(Lower x-values correspond to a more zoomed-out map - level 3 zoom shows the majority of the world, zoom level 5 shows an area roughly the size of North America, level 7 zoom shows an area roughly the size of California, etc.  Decimal values are not currently usable.)


Higher zoom levels show more detail as to where each individual comment/tweet/etc of the collection came from but, of course, shows less of the map as a whole.  Very high zoom levels are only recommended for extremely localized collections.  Trying to zoom in further than level 18 will cause the map to not display.  Zooming out further than level 3 will cause multiple maps of the planet to wrap around to fill the screen BUT images will only appear on one of them - the center one.

---

####Formatting
#####**Base URL:** http://example.com/url/stuff/

---

**Format for a changing a single variable:** 

Reloading the page after changing the base url to

    http://example.com/url/stuff/?z=3

Will change the starting zoom level from 4 to 3

(Note: To reload the page in a way that will keep changes select the url and press the "enter" key.  Do not refresh the page - this will set it back to the previous set of parameters.)


---

**Format for changing multiple variables** (Note: seeing as collections have multiple variables that need to be defined to display correctly this is the most common case.)

Changing multiple parameters is very similar to changing one - additional terms are added on to the end of the url and the page needs to be reloaded for the changes to make effect.  Each additional parameter to be customized needs to be separated by a SINGLE ampersand (&) and no spaces.  For example to change the zoom level to 3 and the starting coordinates of the map to 37.8 degrees North 122 degrees West (roughly the coordinates of San Francisco) one would change the base url to

    http://example.com/url/stuff/?z=3&c=37.8,-122.


Note: There should be NO spaces anywhere in the section of the url where parameters are being defined - they may disrupt the normal functioning of the parameters.

Note: To reload the page in a way that will keep changes select the url and press the "enter" key.  Do not refresh the page - this will set it back to the previous set of parameters.


---

####Instructions for finding variables for the network, Site ID, and Article ID parameters.

**Step numbers correspond to numbers on the screenshot provided - step numbers correspond to labelled parts of the image titled "instructions"**

![Instructions](https://raw.githubusercontent.com/NicholasEM/CustomizableMap/master/Instructions.png)

1) Once on the Livefyre admin console, click on the "Collections" tab.

2) Find the collection you want to use and click on the "embed" tab.

3) Copy the information variables for each parameter you are using - in this example the variables are underlined.

IMPORTANT NOTES: 
You must use ALL THREE of these from the collection for the map to display anything - for example mixing up articleID and siteID WILL cause an error.  Additionally, leaving out one or more of these three parameters will in the best-case scenario display the wrong collection.  However it is more likely that it will just cause an error.

Only copy the parts of the line that are TO THE RIGHT of the '=' sign.

DO NOT copy the quotation marks for any of the information.

For example in the example given for siteID you would copy 347185 and paste that so that part of the url looks like s=347185

You would NOT copy '347185' or siteId: '347185'

At the current moment ALL siteID's are six digits, but that may grow in the future.

ALL THREE of these parameters must be copied from the SAME collection's information - not doing so will almost certainly cause an error.


---


**Other Notes/fixes to common problems**


If far fewer pieces of data are showing up than expected, try zooming in.  At higher zoom levels the map automatically gathers pieces of data from similar geographic areas and represents them with one image on the map along with a number telling how many pieces are in that rough area.

If the map is showing up but there are no pieces of data showing, check the details for the collection you entered and make sure all syntax is completely correct - a single space or number out of place could be causing the problem!


At this point a good way to find the latitude and longitude of a place you want to center the map on is to google "latitude and longitude of   [place]."  

If the map isn't centering where you want it to center remember that North v. South and East v. West are determined by a positive or negative degree value - North/South, East/West, +/- respectively.  Also note that while you DO need a '-' sign in front of the number in order to make the value negative (and correspond to degrees South or West) you DO NOT need a '+' sign in front of the positive numbers.

Again - there should be NO SPACES in the parameter-setting section of the url.  Doing so CAN AND WILL cause an error that will cause the map to not function correctly or not load at all.


