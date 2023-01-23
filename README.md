# How-to-create-3d-Map-of-Indian-city-using-unity
In this repo, we'll be sharing about how to create Indian 3d maps that includes roads, flyovers, tunnels, building etc from open street map data in unity. 
This tutorial is tested on windows 11 on unity verison 2021.3.16f1.git.4200023 and it follows the steps from the VRoads Manual and for more help you can check this  [site](https://vroad.uk/help/).

For this project we need these assets & registry from unity:
* **Global Roads & Traffic** (Lite/Pro) [Link to assets](https://assetstore.unity.com/packages/3d/environments/roadways/global-roads-traffic-lite-218045)
* **Starter Assets - Third Person Character Controller** [Link to Asset](https://assetstore.unity.com/packages/essentials/starter-assets-third-person-character-controller-196526#reviews)
* Unity UI (registry)
* Input system (registry)

## Let's start with the installation steps:
* ### Install Required Package Dependencies
  * Open your project -> window -> package manager -> Unity Registry -> find above mentioned registry and install them (It may lead to restart)
  * From the Package Manager first check that you already have the required packages or not (you can find them into my assets)
  * If not, go to above mentioned links and add them to my assets.
  * In unity, go to window -> package manager -> find above mentioned assets -> download -> import (it may require restart).
* ###  Confirm new Input System
  * Make sure you have the new Input System activated. To check, go to:
    *  Edit -> Project Settings -> Player -> Active Input Handling -> change this to [Input System Handling (New)]
  * Changing this will automatically prompt to a restart.
* ###  Confirm Successful Installation
  * On successful installation, there will be a button on the tools menu named Global Roads & Traffic
 
 
## Quick Start for Maps:
* In unity: Tools -> Global Roads & Traffic
* Open [Pro/Lite] tab -> select [Auto-open scene for tab]
* Open the [Build] tab, select Launch Browser -> It'll prompt to browser.
* Zoom and select any area that fits under the box.
* Find [Copy to Unity] button at the bottom of the page and tap on it, Go back to unity.
* Go to [Build] tab and tap [Play scene 'BuildMap'] (You'll see a progress bar on the scene and game view while it's building, like this) ![map loading page image](https://user-images.githubusercontent.com/87566721/213629539-72092e9b-f173-4458-b5b3-c1929f255919.png)

  * On completion, you can view and move around the map in game view using mouse.
* Now switch to [Traffic] tab 
  *  This will stop the Editor playing and open the RunTraffic scene.
* Click [Play Scene RunTraffic]
  * Once the scene loads, you will see traffic and pedestrians moving.
 
## Steps to follow any vehicle or pedestrian in Play Mode
* Pause the Editor Player (It'll help you to select the vehicle easily)
* Click on a vehicle game object
  * e.g. RunTraffic Scene/ VRoadTraffic/ Cars/ [Select any car number]
* Now play the editor (It'll automatically zoom the map and show you the vehicle running you have selected.)
* example videos: 



https://user-images.githubusercontent.com/87566721/213423763-31b5ea92-7bf0-459d-9d4c-5a873e18c483.mp4




https://user-images.githubusercontent.com/87566721/213424565-15c622eb-c0c6-4e02-a497-2d398c141638.mp4



## Steps to customize the buildings, lanes, junctions in different textures and shapes
* ### For this we need to create Multiple Meshes because earlier the each layer in the scene was a single mesh.
   * For multiple meshes we need to build the map again, but this time, go to the [Options] -> [Create Multiple Meshes] -> [Rebuild] -> tap on [...] -> select cached osm file in json format -> [Play scene 'BuildMap' to rebuild map]. (It'll take some time).
   *  This will create a separate mesh in its own game object for each road, each junction, each building, etc.
   *   You can save meshes for all of the objects to a prefab that you can use later. (optional)
   *   After this you would be able to see mesh for each lane, junction, building, etc like this.![Multple mesh prefab](https://user-images.githubusercontent.com/87566721/213636466-0a377f04-7bbb-43ab-a00f-fabe4ddb71e4.png)

   *    Now you can click on any object and access through hierarchy or just by double click over any object in the map.
 * ### Steps to apply any color over any building
   * Go to [Project] tab -> right click -> create -> materials -> (You can rename the material if you want) -> double click on the material -> go to inspector -> find Main maps -> change color from albedo to whatever you want.
   *  now you can drag this material over any building that you want to apply the same color. The same way you can do for different colors too.

https://user-images.githubusercontent.com/87566721/213659086-cf7b6565-5487-42ec-9094-c8dd53c5edb5.mp4


 * ### Steps to apply any texture over the building
   * Download any texture from Internet.
   * You can find a folder named [materials] in Assets -> VRoad -> Materials. Then drag and drop the downloaded texture into materials folder.
   * Now right click -> create -> materials -> (rename if you want) -> double click on the newly created material -> In Inspector you can find shader at the top -> In shader go to legacy shader -> diffuse. 
   * After this step you'll be able to find select texture option below the color option in inspector. Tap on select texture and select the texture you had dragged into the materials folder.
   * Now you can drag and drop the newly created material (Texture) over any building you want. 

https://user-images.githubusercontent.com/87566721/213662329-4f3a38c2-60a5-4907-8685-50590cf277e9.mp4


 * ### Steps to customize the building shapes and change the number of buildings
   * click on any building from the map you want to customize.
   * You can press 'w' on keyboard to move the building.
   * Press 'E' on keyboard to Rotate the building.
   * Press 'R' on keyboard to resize the buildings.
   * To add more buildings, simply tap on any building and press [command + C] to copy and then [command + V] to paste the building at the same place. Now you can press 'W' and change the position of newly create building and even you can customize the building shape, size and rotation too by using above mentioned steps.


https://user-images.githubusercontent.com/87566721/213665359-dca6bb5d-0fb4-40f9-a472-007f5992bd25.mp4

