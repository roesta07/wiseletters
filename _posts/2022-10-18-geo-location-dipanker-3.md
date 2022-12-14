---
title: "Plotting Plus Codes in Power BI "
last_modified_at: 2022-10-18T16:21:02-05:00
mathjax: true
toc: true
categories:
  - Blog
tags:
  - BI
  - Geolocation
  - python
  - Power BI
  - Plus code
  - Ecommerce
  - Food Delivery
  - Cargo
---

# Plus codes

The Open Location Code (OLC) is a geocode system for identifying an area anywhere on the Earth. Location codes created by the OLC system are referred to as "plus codes". The plus codes are alphanumeric character strings that can be used as address encodings for people or places that do not have addresses and may be especially useful in places where there is no formal system to identify buildings, such as street names, house numbers, and post codes. According to google, billions of people live without an address or an address with low accuracy. 

Plus codes are based on longitude and latitude, however, unlike longitude and latitude they represent a specific area rather than a point whose resolution can be increased or decreased. A code can get more specific if we further divide the grid, adding more characters after the "+" sign, meaning even tiny physical areas like a sidewalk vendor or a street lamp can get their own Plus Code. Alternately, you can remove characters after the "+" sign to get a wider area on the map. Using plus codes, deliveries are receivable, emergency and social services are accessible for everyone. 

Plus codes are convenient as they are derived from latitude and longitude coordinates, which exists everywhere already. Furthermore, their length is similar to that of a telephone or cellphone number. However, they can also be shortened to only four or six digits when combined with a locality (CWC8+R9, Mountain View). Locations close to each other have similar codes. They can completely be encoded or decoded offline. The character set avoids similar looking characters, to reduce confusion and errors, and avoids vowels to make it unlikely that a code spells existing words. Plus codes are not case-sensitive either, and can therefore be easily exchanged over the phone.

Plus codes are increasing being accepted as postal addresses in many parts of the world.

<div > <img src="https://raw.githubusercontent.com/roesta07/wiseletters/master/assets/images/3-geo-location/PlusCodes.png?raw=true" width="820" class="inline"> </div>

Source: <https://maps.google.com/pluscodes/>

## Plus Codes and Power BI

Plus Codes are open source and developed by Google Zurich. Hence, a lot of ecommerce, delivery and other services that use geo location use plus codes to encode addresses in their applications. Ecommerce platforms may use geolocations to identify areas of delivery of customers as well as vendor store locations. Food delivery platforms might use geolocations for similar purposes such as locating their restaurants and food delivery address of their customers. Likewise, cargos, movers and shifters might want to know specific geo-positions of their pickup and drop-off locations. 

The issue occurs when one tries to visualize plus codes in Power BI in order to map these geo locations as a part of their analysis. As of current, unlike longitude and latitude, there is no way to directly visualize plus codes in Power BI. (However, there is a huge possibility that they might be integrated in future versions of Power BI) Therefore, one needs to convert to the plus codes to longitude latitude to plot them in Power BI.
    

<div > <img src="https://raw.githubusercontent.com/roesta07/wiseletters/master/assets/images/3-geo-location/PlusCodesnPowerBI.png?raw=true" width="500" class="inline"> </div>

## Converting Plus Codes to Longitudes and Latitudes

At Wiseyak, we have developed a simple python program (please contact us) to convert plus codes to longitudes and latitudes. This is done using by mapping every single digit of the plus code to corresponding degree in longitude and latitude. With the help of this conversion, we can easily plot the converted longitudes and latitudes in Power BI. 


<div > <img src="https://raw.githubusercontent.com/roesta07/wiseletters/master/assets/images/3-geo-location/Convert1.png" width="820" class="inline"> </div>
<br>
<div > <img src="https://raw.githubusercontent.com/roesta07/wiseletters/master/assets/images/3-geo-location/Convert2.png?raw=true" width="820" class="inline"> </div>
