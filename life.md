# Conway's Game of Life
## AKA Life

Devised by British mathematician John Horton Conway in 1970

## Rules

* Universe = grid
* Squares = dead or alive (states)

Every cell interacts with 8 neighbors

1. live cell < 2 neighbors = die
  * Underpopulation
2. live cell with 2 or 3 neighbors = live
3. live cell > 3 neighbors = die
	* Overcrowding
4. dead cell with 3 neighbors = live
	* Reproduction
	
Conway chose rules meeting these criteria:

1. No explosive growth
2. Patterns with chaotic, unpredictable outcomes
3. Potential for von Neumann universal constructors
4. The rules should be as simple as possible, whilst adhering to the above constraints.

## Interaction
* Initial pattern = seed
* Apply rules continuously
* Each generation = tick

### Zero Player Game
1. Configuration determined by seed
2. No inputs required
3. Each generation is a function of preceding one
3. Observe evolution

## Patterns
* Still Lifes
	* Block
	
	![Block](https://www.evernote.com/shard/s65/sh/baa5d210-e794-453f-a338-47c82b12cee8/9ed5281d522f5f3561f03fa86a25da7d/deep/0/7/3/13%205:49%20PM.png "Block")
	* Beehive
	
	![Beehive](https://www.evernote.com/shard/s65/sh/f970a01a-b5b2-4885-aea7-c19696ad2f6e/65d256275b90516daa7e6cccbbd15afc/deep/0/7/3/13%205:53%20PM.png "Beehive")
	* Loaf
	
	![Loaf](https://www.evernote.com/shard/s65/sh/ca1bb53c-f5b8-45a6-8948-2346a9ef37ca/9834370daddb5251f69120862b4b4678/deep/0/7/3/13%205:55%20PM.png "Loaf")
	* Boat
	
	![Boat](https://www.evernote.com/shard/s65/sh/049f7445-aaf9-41d9-ab15-f16b22029697/e50342200b3f631264e14b0806f6955f/deep/0/7/3/13%206:00%20PM.png "Boat")
* Oscillators (repeating patterns)
	* Blinker
	
	![Blinker](https://www.evernote.com/shard/s65/sh/a9d29664-1c17-4d5f-a21a-949ca2539ad5/2dcf41e9e39dfda858973c795287df70/deep/0/7/3/13%206:03%20PM.png "Blinker")
	* Toad
	
	![Toad](https://www.evernote.com/shard/s65/sh/12f11834-b082-4011-a7cd-5a5bfbc208b4/4931370faefc365c4599afae3e490703/deep/0/7/3/13%206:06%20PM.png "Toad")
	* Beacon
	
	![Beacon](https://www.evernote.com/shard/s65/sh/4963546e-3777-4539-89f7-0c012bb194fc/4236de93f3c11affd4be8bc2c15078cd/deep/0/7/3/13%206:08%20PM.png "Beacon")
	* Pulsar
	
	![Pulsar](https://www.evernote.com/shard/s65/sh/698c4e43-5835-4b7e-9291-ee28e4dcbe28/3e6b67777eb37b509b0c553f7ab587b3/deep/0/7/3/13%206:17%20PM.png "Pulsar")
	

	
* Oscillators (many periods)
	* R-pentomino
	
	![R-pentomino](https://www.evernote.com/shard/s65/sh/af71a780-070d-4b97-8cf8-cd4f6aade6b5/82a4b9782175cae0be7ac5ee2282dcd3/deep/0/7/3/13%206:20%20PM.png "R-pentomino")
	* Diehard
	
	![Diehard](https://www.evernote.com/shard/s65/sh/29f5eea5-433c-416d-a970-d93f2d62c73a/d821c4589f83c0f3a8df7434f094ca8c/deep/0/7/3/13%206:22%20PM.png "Diehard")
	* Acorn
	
	![Acorn](https://www.evernote.com/shard/s65/sh/cec5fe33-9efd-4b9d-a2c8-cfae3754e802/5960c6039e6e55a10b0c8fbbe11155be/deep/0/7/3/13%206:23%20PM.png "Acorn")




* Spaceships (cross board)
	* Glider
	
	![Glider](https://www.evernote.com/shard/s65/sh/367d0faa-09d1-477c-a5ea-4b08ba52d48f/380ccc91b971aa5d4df59c0ac0984b22/deep/0/7/3/13%206:11%20PM.png "Glider")
	* Lightweight
	
	![Lightweight](https://www.evernote.com/shard/s65/sh/b404b606-5fab-4b1c-9775-5ca4e66921c3/eb69b6fe3ab8ff3dcb78d87209b35c3b/deep/0/7/3/13%206:13%20PM.png "Lightweight")

* Guns (add counters)

	![Gosper glider gun](https://www.evernote.com/shard/s65/sh/b13a16cd-9865-42fc-ae7a-3bbd181da013/6a327a2b97237638b03c2735a648a026/deep/0/7/3/13%206:27%20PM.png "Gosper glider gun")
* Puffers (leave trails of smoke)
* Rakes (move and emit spaceships)
* Breeders (leave trails of guns)
* Indefinite Growth
	* ![Indefinite1](https://www.evernote.com/shard/s65/sh/3ca93489-8af0-4277-930e-015ef3970a0e/4ff85fb4b5f3d7bb92d911d0fee0cb00/deep/0/7/3/13%206:30%20PM.png "Indefinite 1")
	* ![Indefinite2](https://www.evernote.com/shard/s65/sh/774d2016-2e33-4610-9a77-516aa56d693f/d60a69a9ff9300566f46ff9b777edd29/deep/0/7/3/13%206:32%20PM.png "Indefinite 2")
	* ![Indefinite3](https://www.evernote.com/shard/s65/sh/e70e54d6-0456-464e-a3ae-d5b829fddb60/c59152ca73c5e559dbe018eb28922777/deep/0/7/3/13%206:36%20PM.png "Indefinite 3")

## Turing Complete

* Counters
* Finite State Machine
* AND, OR and NOT logic gates

This has the same computational power as a universal Turing machine. Anything that can be computed algorithmically can be computed within Life. The game is theoretically powerful as any computer with unlimited memory and no time constraints: it is Turing complete.

A "universal constructor" can be built containing a Turing complete computer, building many types of complex objects, including copies of itself.

## Cellular Automation

* Self Replicating Cell
* "Creating synthetic life"

Rules:

* Reproduce
* Consume energy
* Produce waste

### Resources
* [Processing Sketch](http://www.openprocessing.org/sketch/95216)
* [Wikipedia](http://en.wikipedia.org/wiki/Conway's_Game_of_Life)
* [Life Lexicon](http://www.argentum.freeserve.co.uk/lex_home.htm)



