# shuella
Mapa sembrando huella

<p>A reforestation movement in Guatemala needed an interactive web map displaying information for each reforestation point on a popup.</p>

<p>They needed a simple way to update the information for each point and add points themselves so I created this map that retrieves live data from an editable google spreadsheet.</p>
<h3>Features:</h3>
<ul>
  <li>Retrieves data from google spreadsheet so that they can update it easily with new reforestation points</li>
  <li>Uses Proj4js to project coordinates from a local projection (GTM) to geographical coordinates in WGS84. Coordinates are in GTM on the spreadsheet so they need to be projected to fit leaflets CRS for the markers to be displayed</li>
  <li>Custom icon for markers</li>
  <li>Filters points so that only the ones that fall into Guatemala are displayed (in case coordinates where entered wrongly on the spreadsheet</li>
  <li>Shows popups for each reforestation point. Some list elements are only shown when data is present for that attribute in order to avoid showing "undefined"/"null" when cells are empty in the spreadsheet</li>
</ul>
I used LeafletJS to create the map and turfjs for the geoprocessing (check if points fall inside Guatemala).
