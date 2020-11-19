# Combat State Protocol
The Colosseum combat state protocol is made up of three things:
* The combat state itself
* The local known state
* Combat actions

## Combat State
The combat state is the data which represents combat at a specific atomic timestep and encompasses the following information:
* TODO

## Local Known State
Since an individual player doesn't have a comprehensive picture of the combat state at all times,
there must exist a protocol for determining what a player does and doesn't know.
This is required in order to omit data from what a player should have access to,
such as an opponents health in the event that they shouldn't know it.

Local known state describes this relationship.

## Actions
Actions are the individual atomic operations which modify the combat state.

The possible actions are defined as follows:
* EnterCombat
* ExitCombat
* Attack
* Ability
* Skip
* Forfeit

### Enter Combat
Enter combat is passed to the state when one or more combatants enters the combat state.
This is likely to happen at the start of combat, and in the case of expeditions, when a party member joins another in combat.

### Exit Combat
Exit combat is passed to the state when one or more combatants exits the combat state.
This is used in the event that a player disconnects, or during cinematic events such as boss transformations.

### Attack
Attack is used when a combatant attempts to use the ability associated with their equipable.
This will apply their equipable effects to the supplied targets as specified by their equipable.

### Ability
Ability is used when a combatant attempts to use an ability that they've acquired.
This ability will apply its effects to the targets supplied from its own specifications.

### Skip
Skip does nothing in itself, but anything which modifies the state with each transformation will apply.

### Forfeit
Forfeit is used when a party decides they want to end the game.
The forfeiting party loses and the opposing party is given the win.
The implications of this action are dependant on the context.
