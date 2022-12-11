# Flappy Learning ([Juego](http://keeta67.github.io))

![alt tag](https://github.com/Keeta67/keeta67.github.io/blob/main/img/flappy.png?raw=true)

### Implementacion de [NeuroEvolution.js](http://github.com/Keeta67/keeta67.github.io/blob/main/Neuroevolution.js)
```javascript

var ne = new Neuroevolution({options});

var options = {
    network:[1, [1], 1],    // Perceptron structure
    population:50,          // Population by generation
    elitism:0.2,            // Best networks kepts unchanged for the next generation (rate)
    randomBehaviour:0.2,    // New random networks for the next generation (rate)
    mutationRate:0.1,       // Mutation rate on the weights of synapses
    mutationRange:0.5,      // Interval of the mutation changes on the synapse weight
    historic:0,             // Latest generations saved
    lowHistoric:false,      // Only save score (not the network)
    scoreSort:-1,           // Sort order (-1 = desc, 1 = asc)
    nbChild:1               // number of child by breeding
}

ne.set({options});

var generation = ne.nextGeneration();

ne.networkScore(generation[x], <score = 0>);
```

[Game.js](http://github.com/Keeta67/keeta67.github.io/blob/main/game.js).
