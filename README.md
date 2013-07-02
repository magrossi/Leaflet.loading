Leaflet.loading
===============

Leaflet.loading is a simple loading control for [Leaflet][]. An unobtrusive
loading indicator is added below the zoom control if one exists. The indicator
is visible when tiles are loading or when other data is loading, as indicated by
firing custom events on a map.


## Usage

Include `Control.Loading.js` and create a map with `loadingControl: true` in its
options. Then style your loading indicator. `Control.Loading.css` contains a 
start in this direction. The simplest case would be adding a 16 x 16 loading gif
in `.leaflet-control-loading`.

Once the above is complete you will have a loading indicator that only appears
when tiles are loading. 

If you want to show the loading indicator while other AJAX requests or something
else is occurring, simply fire the `dataloading` event on your map when you 
begin loading and `dataload` when you are finished loading. The control tracks 
the number of concurrent loaders, so it is your responsibility to ensure that 
the `dataloading` and `dataload` are called symmetrically.

### Options

 - **position**: (string) Where you want the control to show up on the map (standard
   Leaflet control option). Optional, defaults to `topleft`
 - **separate**: (boolean) Whether the control should be separate from the zoom
   control or not, defaults to false.
 - **zoomControl**: (L.Control.Zoom) The zoom control that the control should be
   added to. This is only necessary when adding a loading control to a zoom 
   control that you added manually and do not want a separate loading control.


## License

Leaflet.loading is free software, and may be redistributed under the MIT
License.


 [Leaflet]: https://github.com/Leaflet/Leaflet
