# PathFinder
<img src="https://github.com/atharv-patil/pathfinder/assets/83455141/563df622-0de2-4242-b47b-ec433bdafcdb"  width="300" height="300">

## Collaborators
Atharv Patil - [github.com/atharv-patil](https://github.com/atharv-patil)<br>
Utkarsh Shukla - [github.com/utkarshukla7](https://github.com/utkarshukla7)


## Description
PathFinder is a Python application designed to provide efficient route planning for bus transportation using the A* algorithm. It leverages bus stop coordinates obtained from Pune Mahanagar Parivahan Mahamandal Ltd open transit data to calculate the optimal path between two points. By employing the Euclidean distance as a heuristic, PathFinder effectively guides the search for the shortest route.

The application starts by loading the bus stop data from a file called "stops.txt" into a pandas DataFrame. It extracts the coordinates of each bus stop and organizes them into a list for further processing. A distance matrix is then generated using the haversine formula, which calculates the geographical distance between pairs of bus stops. This matrix is saved to a file named "DistanceMatrix.txt" for future reference.

To find the optimal path, PathFinder applies the A* algorithm. It takes the specified start and end bus stops as input and performs a search in a graph-like structure created from the distance matrix. The algorithm intelligently explores the graph, considering both the distance to the goal and the cost incurred so far. Through a series of iterations, it gradually narrows down the search space until it identifies the most efficient route between the two points.

Upon discovering the optimal path, PathFinder presents the results as a list of bus stops that form the route. Each stop is represented by a unique identifier. Additionally, the application visualizes the route on a map using the folium library. The bus stops along the path are marked as red circles, providing a clear and intuitive representation of the recommended route.

PathFinder can be a valuable tool for transportation planners, commuters, and anyone involved in optimizing bus routes. By efficiently calculating the shortest path between bus stops, it can contribute to reducing travel time, improving efficiency, and enhancing the overall bus transportation experience.
## Usage
To use PathFinder, follow the steps below:

1. Download the bus stop data from Pune Mahanagar Parivahan Mahamandal Ltd open transit data.
2. Make sure you have the following dependencies installed:
   - pandas
   - numpy
   - haversine
   - googletrans
   - requests
   - folium
   - geopy
3. Save the bus stop data in a file named "stops.txt" in the project directory.
4. Run the provided code to generate the optimal path between two bus stops.
5. Review the output to obtain the route details.

## Code Explanation
1. The code reads the bus stop data from the "stops.txt" file and stores it in a pandas DataFrame.
2. The bus stops' coordinates are extracted from the DataFrame and stored in a list.
3. A distance matrix is created using the haversine formula to calculate the distance between each pair of bus stops.
4. The distance matrix is saved to a file named "DistanceMatrix.txt".
5. The A* algorithm is used to find the optimal path between the specified start and end bus stops.
6. The route data is processed to determine the stops and connections made along the route.
7. The output is visualized on a map using the folium library, with the bus stops marked as red circles.

## Example Output
An example output of PathFinder is a list of bus stops representing the optimal route between two points.

```
Route: [33884, 33589, 32994, 32868]
```

## Screenshots
![image](https://github.com/atharv-patil/pathfinder/assets/83455141/22f88985-fa25-4403-b574-4ae1b7a4280f)
![image](https://github.com/atharv-patil/pathfinder/assets/83455141/839decdc-a5c5-476e-8fb2-7f4c14cd4951)
![image](https://github.com/atharv-patil/pathfinder/assets/83455141/5e249236-2d4e-4f38-9a69-411d05684bde)



## Acknowledgments
- Pune Mahanagar Parivahan Mahamandal Ltd for providing the open transit data.
- The haversine library for calculating distances between coordinates.
