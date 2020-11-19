# Region State Protocol
The Colosseum region state protocol is made up of two things:
* The region state itself
* Region state actions

## Region State
Region state defines a single instanced region in the game at a specific timestep.
It's designed in a way such that individual state units can be cascaded across a server array, for the sake of load balancing.

This instance state in Colosseum defines the following information:
* TODO

## Actions
Actions are the individual atomic operations which modify the state, and are dependant upon the context of the state.

The possible actions are defined as follows:
* TODO
