###**Customizable Streamhub Map ReadMe**


-----
This app expands on the Streamhub Map application by allowing the user to easily customize the collection displayed by the Streamhub map and certain displays options through the url.

example url: http://example.com/url/stuff/?n=livefyre.com&s=172&a=12345678&z=3

---

####Parameter Definitions

**n=example.com:**  The network of the collection to be displayed.

**s=x:** Sets the Site ID of the collection to be displayed.

**a=y:** Sets the article ID of the collection to be displayed.

**e=anotherexample.com:** Sets the environment for the collection to be displayed (defaults to livefyre.com.)

**c=a,b:** Sets the map's starting center at latitude 'a' and longitude 'b.'

**z=x:** Sets the starting zoom level to x (Lower x-values correspond to a more zoomed-out map.)

---

####Formatting
#####**Base URL:** http://example.com/url/things/

---

**Format for a changing a single variable:** 

Reloading the page after changing the base url to

http://example.com/url/things/?z=3

Will change the starting zoom level from 4 to 3

(Note: To reload the page in a way that will keep changes select the url and press the "enter" key.  Do not refresh the page - this will set it back to the previous set of parameters.)

---

**Format for changing multiple variables** (Note: seeing as collections have multiple variables that need to be defined to display correctly this is the most common case.)

Changing multiple parameters is very similar to changing one - additional terms are added on to the end of the url and the page needs to be reloaded for the changes to make effect.  Each additional parameter to be customized needs to be seperated by a single ampersand (&) and no spaces.  For example to change the zoom level to 3 and the starting coordeinates of the map to 37.8 degrees North 122 degrees West (roughly the coordinates of San Francisco) one would change the base url to

http://example.com/url/things/?z=3&c=37.8,-122.

---





