# Ant-Colony-Simulation
## About the demo
This is an AI project I developed with a colleague of mine while at uni. It's a simulation of the foraging behavior of an ant colony.

Ants have limited vision and hearing, but they have extremely good odor sensing capabilities, so in order to navigate their environment they leave trails of chemical substances behind called pheromones for the rest of the colony to sense. Ants that are leaving the nest in search of food will leave "nest" (blue) pheromones behind, while ants carrying food will leave "food" (green) pheromones behind. In turn, each ant will go in the direction where they sense a stronger presence of the pheromone type they're interested in.

(Explain path optimization)

(Explain placing of food sources and walls)

This method of inter-agent communication is called "stigmergy", where each agent in a group modifies the environment in order to guide decision making of other agents. It hasn't been explored that much in videogames but it is an interesting topic.

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

## Implementation details
(Add implementation details)
