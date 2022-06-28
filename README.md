# ARpi_SBB
## SBB Challenge AR Navigation System

### Team:
Cao-Tri Do <br>
Mirella Haldimann <br>
Klaus Fuchs


### Problem statement
Finding the correct path within and around a complex train station is hard. Especially when path-finding involves the change in mode of transport. Fast and accurate transfers are key to a convenient and efficient connection. This situation becomes all the more pertinent when travellers are under time pressure or unfamiliar with the local public transport eco-system.
Lack of GPS or bluetooth enabled beacons/smartphones compound this issue and make in- and outer-station navigation a technical challenge.
For this, it is necessary to improve travel conditions for passengers that need to find the train/bus/tram as fast as they can and reduce time to look at the map or orient. In order to improve navigation (under stress and time constraint) the passenger selects the train he wants to get on and “a system” will give guidance

### Our Solution
Allows to navigate 3 different routes but can be easily extended to more
Allows integration of train-relevant information, such as the departure times. The app then can integrate signaling whether a path to a connection on a certain platform is reachable (green) or requires a fast sprint (yellow) or is unreachable (red).

### Software
Unity SDK 2019.2.0f1 Personal  (https://unity3d.com/get-unity/download)
Placenote AR SDK: SImply a tool to store waypoints coordinate after saving them in a database (https://placenote.com/docs/downloads/ )
Our work is based on previous efforts in AR navigation https://github.com/MatthewHallberg/IndoorNavPlaceNote

### Hardware
Ipad iOS 11 on Macbook Pro (version: Mojave 10.14.6)

### Techstack
- 3D Modeling and rigid body transformation
- Augmented Reality Technology: Apple ARkit
- Software development in C#, xCode
- Unity
- User Interface + Usability

### 2 step Procedure

- We need to get the waypoints first, save them into the cloud database of Placenote and use them to lead the person from Start A to Destination B. For this, we will run an app “createMap” and walk along the path and finally set a destination point at the end. After saving the map the relevant points are transferred to the cloud database.


- Then when the area is scanned, we will use this information to feed it into a second app “ReadMap” which will then receive the waypoint locations and create a path from start A to destination B.



### Limitations

Our prototype that we developed is not yet suitable for real-world scenarios. We have tried to use the app at the train station but failed in localizing the environment. This could be due to:
Wide pathways and few edges resulted in unstable tracking of the environment when using visual positioning algorithm
A lot of transparent surfaces (e.g. glass windows) led to 
Suggestion: The amount of information for the tracking may be not sufficient, therefore the inclusion of landmarks (through Beacon technology which is already available at the train station) or prior knowledge about the environment (through 3D map of the train station)
We have not showcased a scenario for multi-level navigation (moving between floors) but this should not invoke any problems as the visual positioning can handle this issue
Light conditions may have an influence in accurate tracking/localizing of the waypoints

### Future outlook

Usability of the app: Not showcased in the presentation but implemented, we further developed a prototypical user-interface  in case the passenger has missed her/his connections when arriving at the destination transfer. A display appears that shows the upcoming possibilities. This will further integrate the SBB API to allow for live synchronous updates. Additionally, the color of the arrows should change dynamically (from green to red) relative to the time needed and until transportation departures. 
The additional usage of the Beacon technology could help to improve in an ‘comfortable’’ spread of people at the train station. For instance, through infrared sensoring it could be determined which areas are more densed than others and thus this would give the app additional options for re-routing such that the user can more efficiently walk to his/her destination
Another point of interest, is to consider personalized navigation. In our current approach, we made simple scenarios assuming that the route is easily walkable, however, this may not always be the case, when considering people in wheelchairs or people with lots of baggage. In the aforementioned scenario, it will, for example 

