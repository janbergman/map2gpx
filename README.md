# Map2GPX

Turn an orienteering map with a printed course into a georeferenced KMZ and GPX control points. Runs in your browser as a single HTML file, with instructions at the bottom of the map.

**[Open Map2GPX](https://janbergman.github.io/map2gpx/map2gpx.html)** · **[Instructions and example](https://janbergman.github.io/map2gpx/)**

# Orienteering training run
Use the app **[EasyTrails](https://www.easytrailsgps.com)** and download the .gpx file to get a beep when you are close to any controls (in any order).

### Run with GPX in EasyTrails

Unzip the Map2GPX download, transfer the **_course.gpx** file to your iPhone, and open/import it in EasyTrails as waypoints. Enable waypoint proximity alarms in EasyTrails to receive an alert near a control. The points have no required visit order. See the [EasyTrails features](https://www.easytrailsgps.com/features/) for waypoint import and proximity alarms.

### Start Map2GPX

Click **Open Map2GPX** above to run it online. Alternatively download **map2gpx.html** and double-click it to open it in Safari or Chrome. No installation is required. Use **O** to open your map and **S** to save; **H** shows help.


## Getting started

1. Click the welcome screen or press **O**. Open a calibrated **KMZ** (for example from Livelox), or a **JPG/PNG** map with a printed course.
2. For an uncalibrated image, select a recognizable point in the image and the same place in OpenTopoMap. **G** searches for a place or accepts latitude, longitude. **Tab** switches between the image and background map.
3. For an uncalibrated image, drag a blue image corner to adjust scale and rotation around the anchor. Check alignment at several places. **S** downloads a calibrated map copy named **…_map.kmz**. An already calibrated KMZ keeps its calibration and goes straight to selecting the start, without saving another copy.
4. Click the centre of the start triangle. **If there is no start triangle, press N to skip directly to selecting a control ring.** No artificial start point is added.
5. Click the centre of any control circle. **Zoom in until the printed colour is clearly visible, then click in the middle of the coloured ring stroke where the map background is white.** Radius and colour are sampled together; scanning starts automatically.
6. Review the small blue markers. **S** downloads a ZIP containing both **KMZ and GPX**. Unzip it in Finder or your file manager.

**GPX always contains independent waypoints, without course order, route or track.** Labels such as K01 identify points, not the order in which to visit them. No OCR is performed. Additional start triangles are detected automatically, and you can add starts manually.

## Keyboard and mouse

| Action | Command |
| --- | --- |
| Zoom | Scroll/pinch or **+ / −** |
| Pan | Drag empty map, or hold **Space** and drag |
| Fit the map | **F** |
| Full screen | **F11**, or the browser's View menu; Mac may require **Fn** |
| Search place / coordinates | **G** |
| Add a control after scanning | Click an empty place |
| Select / move a point | Click / drag its marker |
| Delete selected point | **Delete / Backspace** |
| Undo, including a rescan | **Cmd+Z / Ctrl+Z** |
| Choose a new ring sample and rescan | **R** |
| Reselect first start / add another start | **T / Shift+T** |
| Continue without a start triangle | **N** at the start-selection step |
| Choose a new geographic anchor | **A** |
| Open / save | **O / S** |
| Cancel / help | **Esc / H** |
| Retry background tiles | **L** |

## Local use and privacy

Only **map2gpx.html** is needed to run the program. Download that file and open it in a modern browser; no Python, installation or local server is required. The file is about 15 MB because OpenCV and its WebAssembly code are bundled inside it.

Your map image, detection and export are processed locally in the browser. Internet access is needed for OpenTopoMap and place search. Original map files are not modified. Keep your exported KMZ: it includes the original image and editable points, so you can reopen your work.

Opening a file and entering full screen are separate actions. Use **F11** after opening the file. On the GitHub file page, use **Download raw file** to obtain the standalone HTML.


## Svenska – kort handledning

Öppna programmet och följ statusraden längst ned. **O** öppnar karta och **S** sparar. För JPG/PNG förankrar du först en bildpunkt mot samma plats i OpenTopoMap, justerar med hörnen och sparar kartan. Markera sedan starten, eller tryck **N** om starttriangel saknas. Välj därefter ett kontrollcentrum och ringkanten. **Zooma in och klicka mitt i den färgade ringkanten där kartbakgrunden är vit.** Skanningen startar automatiskt. Granska, rätta vid behov och spara ZIP-filen med KMZ och GPX. Kontrollerna sparas alltid utan banordning. **R** väljer ny ringmall och skannar om; **Cmd+Z** ångrar.

## Libraries and map credits

Uses [OpenCV 4.13.0](https://docs.opencv.org/4.13.0/) (Apache 2.0) and [fflate 0.8.2](https://github.com/101arrowz/fflate/tree/v0.8.2) (MIT); their licenses are embedded in the HTML. Background map: © OpenStreetMap contributors, SRTM and OpenTopoMap (CC-BY-SA). Example map artwork remains the property of its respective rights holders; the screenshot illustrates the program's output.
