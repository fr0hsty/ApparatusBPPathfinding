# ApparatusBPPathfinding

This repo provides one example way of creating agents capable of finding paths to destinations using Apparatus and BP.

// Could also just store one component with an Enum containing the state of the agent between desires path, pathing, and finished pathing, etc.

Traits:
- Position
- DesiredVelocity
- Desires path (Has destination vector)
- Pathing (has path points)
- FinishedPath (Binary flag)

Mechanics:

Mechanic - Findpaths
Include DesiresPath
Include Position
Determine path points from A to B. Not sure how to handle path failure.

Mechanic - SetDesiredVelocity
Include HasPath
Exclude FinishedPath.
Determine desired velocity via points, remove points if within some tollerance, and add finished path trait if pathing is done.

Mechanic - MoveAgents
Include DesiredVelocity
Include Position
Add desired velocities onto all positions.

https://user-images.githubusercontent.com/17767740/150754106-2fcc0d1a-11c7-4cf9-8871-ba4268a81088.mov

