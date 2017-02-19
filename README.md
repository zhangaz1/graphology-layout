[![Build Status](https://travis-ci.org/graphology/graphology-layout.svg)](https://travis-ci.org/graphology/graphology-layout)

# Graphology Layout

Collection of basic layout algorithms to be used with [`graphology`](https://graphology.github.io).

## Installation

```
npm install graphology-layout
```

## Usage

* [circular](#circular)
* [random](#random)

### #.circular

Arranges the node in a circle.

*Example*

```js
import {circular} from 'graphology-layout';
// Alternatively, to load only the relevant code:
import circular from 'graphology-layout/circular';

const positions = circular(Graph);

// With options:
const positions = circular(Graph, {scale: 100});

// To directly assign the positions to the nodes:
circular.assign(Graph);
```

*Arguments*

* **graph** *Graph*: target graph.
* **options** *?object*: options:
  - **attributes** *?object*: attributes to map:
    + **x** *?string* [`x`]: name of the x position.
    + **y** *?string* [`y`]: name of the y position.
  - **center** *?number* [`0.5`]: center of the layout.
  - **scale** *?number* [`1`]: scale of the layout.

### #.random

Random layout positionning every node by choosing each coordinates uniformly at random on the interval `[0, 1)`.

*Example*

```js
import {random} from 'graphology-layout';
// Alternatively, to load only the relevant code:
import random from 'graphology-layout/random';

const positions = random(Graph);

// With options:
const positions = random(Graph, {rng: customRngFunction});

// To directly assign the positions to the nodes:
random.assign(Graph);
```

*Arguments*

* **graph** *Graph*: target graph.
* **options** *?object*: options:
  - **attributes** *?object*: attributes to map:
    + **x** *?string* [`x`]: name of the x position.
    + **y** *?string* [`y`]: name of the y position.
  - **center** *?number* [`0.5`]: center of the layout.
  - **rng** *?function* [`Math.random`]: custom RNG function to use.
  - **scale** *?number* [`1`]: scale of the layout.
