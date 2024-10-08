# How-to-create-3d-Map-of-Indian-city-using-unity
In this repo, we'll be sharing about how to create Indian 3d maps that includes roads, flyovers, tunnels, building etc from open street map data in unity.

For this project we need these assets & registry from unity:
* **Global Roads & Traffic** (Lite/Pro) [Link to assets](https://assetstore.unity.com/packages/3d/environments/roadways/global-roads-traffic-lite-218045)
* **Starter Assets - Third Person Character Controller** [Link to Asset](https://assetstore.unity.com/packages/essentials/starter-assets-third-person-character-controller-196526#reviews)
* Unity UI (registry)
* Input system (registry)

## Let's start with the installation steps:
* ### Install Required Package Dependencies
  * windows -> package manager -> Unity Registry -> find above mentioned registry and install them (It may lead to restart)
  * From the Package Manager first check that you already have the required packages or not (you can find them into my assets)
  * If not, go to above mentioned links and add them to my assets.
  * In unity, go to windows -> package manager -> find above mentioned assets -> download -> import it may require restart.
* ###  Confirm new Input System
  * Make sure you have the new Input System activated. To check, go to:
  * Edit -> Project Settings -> Player -> Active Input Handling -> change this to [Input System Handling (New)]
  * Changing this will automatically prompt to a restart.
* ###  Confirm Successful Installation
  * On successful installation, there will be a button on the tools menu named Global Roads & Traffic
 
 
## Quick Start for Maps:
* In unity: Tools -> Global Roads & Traffic
* Open [Pro/Lite] tab -> select Auto-open scene for tab
* Open the [Build] tab, select Launch Browser -> It'll prompt to browser.
* Zoom and select any area that fits under the box.
* Find [Copy to Unity] button at the bottom of the page and tap on it, Go back to unity.
* Go to [Build] tab and tap [Play scene 'BuildMap'] (You'll see a progress bar on the scene and game view while it's building)
  * On completion, you can view and move around the map in game view using mouse.
* Now switch to [Traffic] tab 
  *  This will stop the Editor playing and open the RunTraffic scene.
* Click [Play Scene RunTraffic]
  * Once the scene loads, you will see traffic and pedestrians moving.

