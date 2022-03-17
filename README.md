<p align="center"><img src="PyLandGuessrBanner.jpg"\></p>

# PyLandGuessr
* PylandGuessr is a programm that allows you to guess country with an image like the game GeoGuessr.

# Requirement
* pygame
* geopy
* numpy
* open-cv

# How to play
* Once lauched, an image is randomly selected
* A window with the world map appears
* You have to click on the country where you think the image belongs
  * If you guess the right country you win.
  * If you don't guess but still have some attempts left, the program shows you the distance and direction to which the country is located 
  * If you don't guess and you have no more attempts left, you have lost.
  
# How it work
* The window size is 1200*600
* The mouse position is converted to X and Y in this window
* Position X = 0 and Y = 0 is equivalent to longitude = 0 and latitude = 0
<p align="center"><img src="images/ImageReadme/geolocalisationLat0Lon0.jpg"\></p>
* X and Y are converted into Lon and Lat using coefficients calculated by me (the precision is not perfect, see excel)
<p align="center"><img src="images/ImageReadme/LatitudeLongitude.jpg"\></p>
* The name of the image (country) is stored in the program
* The program keeps the geolocation of the country of the image for when the player makes a wrong prediction
* The geolocation proposed by the player is converted into a country if it corresponds to one of them
  *  If the country proposed is the same as the one in the image, then it's a winner
  *  If the proposed country is not the same and if there are any attempts left, then the program calculates the distance between the proposed country and the searched one and adds the direction (cardinal point) where it is located.
  
# Images of the game
