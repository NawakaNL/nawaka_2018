


Bekijk alle deelnemende groepen op de kaart
--------------------------------------------





 Gepubliceerd: zaterdag 23 januari 2021 18:04
   




 Ben je benieuwd waar alle deelnemende scoutinggroepen vandaan komen? Kijk dan snel op de onderstaande kaart. Ben je benieuwd wie er nog meer op je subkamp staan? Kijk dan snel
 [op je subkamppagina](/nl/deelnemers/subkampen) 
 .
 



 Je kunt het overzicht van deelnemende groepen ook downloaden. Kijk daarvoor bij
 [downloads voor deelnemers](/nl/deelnemers/voorwaarden-en-kampregels) 
 .
 


 START: Modules Anywhere 






 mapboxgl.accessToken = 'pk.eyJ1IjoidHJpc3RhbmRiIiwiYSI6ImNqY3EwMHUzbjI1d2kycW14amljbjllcXoifQ.E3Xy13d6hn3e9nh0jFejZA';
var map = new mapboxgl.Map({
 container: 'groepherkomst',
 center: [5.291266, 52.232633],
 zoom: 7,
 style: 'mapbox://styles/mapbox/streets-v10'
});

map.on('load', function () {
 // Add a new source from our GeoJSON data
 map.addSource("groups", {
 type: "geojson",
 cluster: false,
 clusterMaxZoom: 14,
 clusterRadius: 50,
 data: "http://nawaka.scouting.nl/modules/mod\_groepherkomst/tmpl/groups.geojson"
 });

 
 // Add Nawaka Logo
 map.loadImage('http://nawaka.scouting.nl/modules/mod\_groepherkomst/images/nawaka.jpg', function(error, image) {
 if (error) throw error;
 map.addImage('nawaka', image);
 map.addLayer({
 "id": "nawaka",
 "type": "symbol",
 "source": {
 "type": "geojson",
 "data": {
 "type": "FeatureCollection",
 "features": [{
 "type": "Feature",
 "geometry": {
 "type": "Point",
 "coordinates": [5.519, 52.2847]
 }
 }]
 }
 },
 "layout": {
 "icon-image": "nawaka",
 "icon-size": 0.20
 }
 });
 });

 // Load every subkamp (as source)
 // Loads image for subkamp
 map.loadImage('http://nawaka.scouting.nl/modules/mod\_groepherkomst/images/rif.png', function (error, image) {
 if (error) throw error;
 map.addImage("Rif", image);
 });

 // Adds a layer for the subkamp
 map.addLayer({
 id: "groups-Rif",
 type: "symbol",
 source: "groups",
 filter: ["==", "subkamp", "Rif"],
 layout: {
 "icon-image": "Rif",
 "icon-size": 0.5
 }
 });

 // Adds onclicklistener for subkamp groups
 map.on('click', 'groups-Rif', function (e) {
 new mapboxgl.Popup()
 .setLngLat(e.features[0].geometry.coordinates)
 .setHTML('<h3>'+e.features[0].properties.title + '</h3> Subkamp '
 + e.features[0].properties.subkamp + '<br/>' +
 e.features[0].properties.description)
 .addTo(map);
 });

 // Change the cursor to a pointer when the mouse is over the places layer.
 map.on('mouseenter', 'groups-Rif', function () {
 map.getCanvas().style.cursor = 'pointer';
 });

 // Change it back to a pointer when it leaves.
 map.on('mouseleave', 'groups-Rif', function () {
 map.getCanvas().style.cursor = '';
 });
 // Loads image for subkamp
 map.loadImage('http://nawaka.scouting.nl/modules/mod\_groepherkomst/images/oase.png', function (error, image) {
 if (error) throw error;
 map.addImage("Oase", image);
 });

 // Adds a layer for the subkamp
 map.addLayer({
 id: "groups-Oase",
 type: "symbol",
 source: "groups",
 filter: ["==", "subkamp", "Oase"],
 layout: {
 "icon-image": "Oase",
 "icon-size": 0.5
 }
 });

 // Adds onclicklistener for subkamp groups
 map.on('click', 'groups-Oase', function (e) {
 new mapboxgl.Popup()
 .setLngLat(e.features[0].geometry.coordinates)
 .setHTML('<h3>'+e.features[0].properties.title + '</h3> Subkamp '
 + e.features[0].properties.subkamp + '<br/>' +
 e.features[0].properties.description)
 .addTo(map);
 });

 // Change the cursor to a pointer when the mouse is over the places layer.
 map.on('mouseenter', 'groups-Oase', function () {
 map.getCanvas().style.cursor = 'pointer';
 });

 // Change it back to a pointer when it leaves.
 map.on('mouseleave', 'groups-Oase', function () {
 map.getCanvas().style.cursor = '';
 });
 // Loads image for subkamp
 map.loadImage('http://nawaka.scouting.nl/modules/mod\_groepherkomst/images/bermuda.png', function (error, image) {
 if (error) throw error;
 map.addImage("Bermuda", image);
 });

 // Adds a layer for the subkamp
 map.addLayer({
 id: "groups-Bermuda",
 type: "symbol",
 source: "groups",
 filter: ["==", "subkamp", "Bermuda"],
 layout: {
 "icon-image": "Bermuda",
 "icon-size": 0.5
 }
 });

 // Adds onclicklistener for subkamp groups
 map.on('click', 'groups-Bermuda', function (e) {
 new mapboxgl.Popup()
 .setLngLat(e.features[0].geometry.coordinates)
 .setHTML('<h3>'+e.features[0].properties.title + '</h3> Subkamp '
 + e.features[0].properties.subkamp + '<br/>' +
 e.features[0].properties.description)
 .addTo(map);
 });

 // Change the cursor to a pointer when the mouse is over the places layer.
 map.on('mouseenter', 'groups-Bermuda', function () {
 map.getCanvas().style.cursor = 'pointer';
 });

 // Change it back to a pointer when it leaves.
 map.on('mouseleave', 'groups-Bermuda', function () {
 map.getCanvas().style.cursor = '';
 });
 // Loads image for subkamp
 map.loadImage('http://nawaka.scouting.nl/modules/mod\_groepherkomst/images/palmeiland.png', function (error, image) {
 if (error) throw error;
 map.addImage("Palmeiland", image);
 });

 // Adds a layer for the subkamp
 map.addLayer({
 id: "groups-Palmeiland",
 type: "symbol",
 source: "groups",
 filter: ["==", "subkamp", "Palmeiland"],
 layout: {
 "icon-image": "Palmeiland",
 "icon-size": 0.5
 }
 });

 // Adds onclicklistener for subkamp groups
 map.on('click', 'groups-Palmeiland', function (e) {
 new mapboxgl.Popup()
 .setLngLat(e.features[0].geometry.coordinates)
 .setHTML('<h3>'+e.features[0].properties.title + '</h3> Subkamp '
 + e.features[0].properties.subkamp + '<br/>' +
 e.features[0].properties.description)
 .addTo(map);
 });

 // Change the cursor to a pointer when the mouse is over the places layer.
 map.on('mouseenter', 'groups-Palmeiland', function () {
 map.getCanvas().style.cursor = 'pointer';
 });

 // Change it back to a pointer when it leaves.
 map.on('mouseleave', 'groups-Palmeiland', function () {
 map.getCanvas().style.cursor = '';
 });
 // Loads image for subkamp
 map.loadImage('http://nawaka.scouting.nl/modules/mod\_groepherkomst/images/waterval.png', function (error, image) {
 if (error) throw error;
 map.addImage("Waterval", image);
 });

 // Adds a layer for the subkamp
 map.addLayer({
 id: "groups-Waterval",
 type: "symbol",
 source: "groups",
 filter: ["==", "subkamp", "Waterval"],
 layout: {
 "icon-image": "Waterval",
 "icon-size": 0.5
 }
 });

 // Adds onclicklistener for subkamp groups
 map.on('click', 'groups-Waterval', function (e) {
 new mapboxgl.Popup()
 .setLngLat(e.features[0].geometry.coordinates)
 .setHTML('<h3>'+e.features[0].properties.title + '</h3> Subkamp '
 + e.features[0].properties.subkamp + '<br/>' +
 e.features[0].properties.description)
 .addTo(map);
 });

 // Change the cursor to a pointer when the mouse is over the places layer.
 map.on('mouseenter', 'groups-Waterval', function () {
 map.getCanvas().style.cursor = 'pointer';
 });

 // Change it back to a pointer when it leaves.
 map.on('mouseleave', 'groups-Waterval', function () {
 map.getCanvas().style.cursor = '';
 });
 // Loads image for subkamp
 map.loadImage('http://nawaka.scouting.nl/modules/mod\_groepherkomst/images/aan de haven.png', function (error, image) {
 if (error) throw error;
 map.addImage("aan de haven", image);
 });

 // Adds a layer for the subkamp
 map.addLayer({
 id: "groups-aan de haven",
 type: "symbol",
 source: "groups",
 filter: ["==", "subkamp", "aan de haven"],
 layout: {
 "icon-image": "aan de haven",
 "icon-size": 0.5
 }
 });

 // Adds onclicklistener for subkamp groups
 map.on('click', 'groups-aan de haven', function (e) {
 new mapboxgl.Popup()
 .setLngLat(e.features[0].geometry.coordinates)
 .setHTML('<h3>'+e.features[0].properties.title + '</h3> Subkamp '
 + e.features[0].properties.subkamp + '<br/>' +
 e.features[0].properties.description)
 .addTo(map);
 });

 // Change the cursor to a pointer when the mouse is over the places layer.
 map.on('mouseenter', 'groups-aan de haven', function () {
 map.getCanvas().style.cursor = 'pointer';
 });

 // Change it back to a pointer when it leaves.
 map.on('mouseleave', 'groups-aan de haven', function () {
 map.getCanvas().style.cursor = '';
 });
 // Loads image for subkamp
 map.loadImage('http://nawaka.scouting.nl/modules/mod\_groepherkomst/images/aan de gracht.png', function (error, image) {
 if (error) throw error;
 map.addImage("aan de gracht", image);
 });

 // Adds a layer for the subkamp
 map.addLayer({
 id: "groups-aan de gracht",
 type: "symbol",
 source: "groups",
 filter: ["==", "subkamp", "aan de gracht"],
 layout: {
 "icon-image": "aan de gracht",
 "icon-size": 0.5
 }
 });

 // Adds onclicklistener for subkamp groups
 map.on('click', 'groups-aan de gracht', function (e) {
 new mapboxgl.Popup()
 .setLngLat(e.features[0].geometry.coordinates)
 .setHTML('<h3>'+e.features[0].properties.title + '</h3> Subkamp '
 + e.features[0].properties.subkamp + '<br/>' +
 e.features[0].properties.description)
 .addTo(map);
 });

 // Change the cursor to a pointer when the mouse is over the places layer.
 map.on('mouseenter', 'groups-aan de gracht', function () {
 map.getCanvas().style.cursor = 'pointer';
 });

 // Change it back to a pointer when it leaves.
 map.on('mouseleave', 'groups-aan de gracht', function () {
 map.getCanvas().style.cursor = '';
 });
 
 });
 
 END: Modules Anywhere 


