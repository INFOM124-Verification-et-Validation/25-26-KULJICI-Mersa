# Specification-based Testing (Exercise 1)

## 1. Goal, inputs and outputs
- Goal: Tries to calculate a move based on the behaviour of the npc.
- Input domain: map, joueur et position de clyde
- Output domain: Direction ou empty (car **optionnel**)

## 2. Explore the program (if needed)

## 3. Identify input and output partitions

### Input partitions

#### Individual inputs
Distance partitions:
- D1: Clyde is within 8 grid spaces of Pac-man (distance < 8)
- D2: Clyde is beyond 8 gris spaces of Pac-man (distance > 8)
- D3: Clyde is at exactly 8 grid spaces of Pac-man (distance = 8)

Pac-man not on the board

Pac-man at the edge of the board

Pac-man does not have a square

Obstacle direction partitions:
- D1: Path of Clyde is free
- D2: Path of Clyde is blocked
- D3: Clyde is on Pac-man
- Clyde has multiple valid moves

Not valid maps:
- Multiple Clydes on the map
- Multiple Pac-men on the map

#### Combinations of input values
- Distance < 8 & path free
- Distance < 8 & path blocked
- Distance < 8 & multiple moves

- Distance > 8 & path free
- Distance > 8 & path blocked
- Distance > 8 & multiple moves
-
- Distance = 8 & path free
- Distance = 8 & path blocked
- Distance = 8 & multiple moves

### Output partitions
- Empty direction
- Direction towards Pac-man 
- Direction away from Pac-man

## 4. Identify boundaries
Invalid cases: 
- Multiple Clydes on the map
- Multiple Pac-men on the map 
- Clyde is on Pac-man 
- Clyde does not have a square partition
- Pac-man does not have a square partition

Pac-man at the edge of the board partition

Pac-man goes from one edge of the map to the other 

## 5. Select test cases

Distance < 8: 
- Test 1: Path free => Direction away from Pac-man
- Test 2: Path blocked => Empty direction 
- Test 3: Multiple moves => Direction away from Pac-man

Distance > 8: 
- Test 4: Path free => Direction towards Pac-man 
- Test 5: Path blocked => Empty direction 
- Test 6: Multiple moves => Direction towards Pac-man

Distance = 8: 
- Test 7: Path free => 
- Test 8: Path blocked =>
- Test 9: Multiple moves =>

Boundaries: 
- Test 10: Multiple Clydes on the map => 
- Test 11: Multiple Pac-men on the map => 
- Test 12: Clyde is on Pac-man => 
- Test 13: **Clyde does not have a square partition** => 
- Test 14: **Pac-man does not have a square partition** => 