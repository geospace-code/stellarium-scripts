# Stellarium .ssc example scripts

Stellarium can be used repeatably via ECMAScript [.ssc scripts](https://stellarium.org/doc/0.19/scripting.html).
Here are a few relevant parameters.

FOV = field of view.

```javascript
LabelMgr.deleteAllLabels()  // clear off any labels that clutter view
core.setDate("2000-01-23T04:45:15","utc",true)  // use UTC time
core.setTimeRate(0)  // do not advance time, pause at the specified time
StelMovementMgr.zoomTo(FOV_degrees, 0)  //0 disables zoom animation
core.setObserverLocation(lon, lat, alt_meters, 0, "myName")  // 0 disables move animation
core.moveToRaDecJ2000(RA,DEC,0)  // move to right ascension, declination :  0=without animation
core.setDiskViewport(false)  // use full window, not a simultated circular lens
```

Turn on azimuthal and equatorial grids:

```javascript
GridLinesMgr.setFlagAzimuthalGrid(true)
GridLinesMgr.setFlagEquatorGrid(true)
```

Turn on constellation lines and labels

```javascript
ConstellationMgr.setFlagLines(true)
ConstellationMgr.setFlagLabels(true)
```

Turn on compass cardinal points (NESW) and turn off landscape

```javascript
LandscapeMgr.setFlagCardinalsPoints(true)
LandscapeMgr.setFlagLandscape(false)
```