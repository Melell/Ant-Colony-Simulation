# Ant-Colony-Simulation
## About the demo
This is an AI project I developed with a colleague of mine while at uni. It's a simulation of the foraging behavior of an ant colony.

Ants have limited vision and hearing, but they have extremely good odor sensing capabilities, so in order to navigate their environment they leave trails of chemical substances behind called pheromones for the rest of the colony to sense. Ants that are leaving the nest in search of food will leave "nest" (blue) pheromones behind, while ants carrying food will leave "food" (green) pheromones behind. In turn, each ant will go in the direction where they sense a stronger presence of the pheromone type they're interested in.

Pheromones will evaporate over time, and the intensity of the pheromones dropped decreases over time unless ants go over the nest or food source again. This means that if ants form long paths between the nest and food source, it will eventually be optimized to be as short as possible because shorter paths will have stronger pheromone intensities.

<img src="imgs/AntSimulationSnippet.gif" alt="GIF showing the simulation with ants optimizing the path formed to between food and nest over time." width="480" height="270" />

In our demo, we implement all these concepts and allow the user to place the nest and food anywhere. We also give the ability to add/remove walls while the simulation is running, to force ants on different paths. For more details on how the demo was implemented please refer to the document attached to the release.

This method of inter-agent communication is called "stigmergy", where each agent in a group modifies the environment in order to guide decision making of other agents. It is a very interesting idea that hasn't been explored that often in videogames.

## Camera controls (spherical camera)
  - Q/E Keys: Zoom out/zoom in
  - A/D: Rotate left/right around center point
  - S/W: Rotate down/up around center point

## Editor options
### Level edit options
- Nest mode: Left click on level to place the nest (only first time) and start the simulation
- Food mode: Hold left mouse button to drop cubes of food around the level
- Wall mode: Hold left mouse button to add walls, hold right mouse button to remove walls

### Simulation parameters
NOTE: While these parameters are exposed for the user to play around, they've been configured to give good results. Any other values could result in ants having difficulty establishing good paths to the food sources.

- Number Of Ants: Add/remove ants from the simulation (this will reset the simulation, removing all walls and food already placed!)
- Pause Simulation checkbox: When checked, everything will be paused, but you can still place food/walls
- Reset Simulation: Eliminate all ants, nest, food, walls etc and restart all the ants' properties
- Drop Pheromone Time: The time interval between each pheromone drop of ants
- Pheromone Decision Time: The time interval between each decision that an ant takes of which direction to follow based on the pheromone concentration ahead
- Ant FOV Radius: The radius of the ants' FOV
- Pheromone Time: The time it takes for a pheromone dropped to completely evaporate
