## Lecture 2 & 3: Behaviour-Based Robotics

### Why Study Biological Sciences for Robotics?

- Animals and humans provide existence proofs of different aspects of intelligence

- Even “simple” animals (insects, fish, frogs) exhibit intelligent behaviour while at the same time overcoming the closed world assumption.

- Animal studies can provide models that a roboticist can operationalize within a robotic system
  - Models can be implemented with high fidelity to animal counterparts (biologically realistic), or,
  - Models may serve only as inspiration for the robotics researcher



### What is “Behaviour”?

Mapping of sensory inputs to a pattern of motor actions that are used to achieve a task.



### Innate Releasing Mechanisms (IRMs)

a combination of stimuli that elicit a specific, perhaps complex, response to a particular biological situation

<img src="/Users/dahao/pmlb/robotics/COP518-Robotics-Notes/figures/02-irms.png" alt="image-20200128211416837" style="zoom:50%;" />



#### Releaser

- Similar to a latch or Boolean variable that has to be set by a stimulus

- Acts as a control signal to activate a behavior 



### Schema Theory

Way of expressing basic unit of activity

#### Schema:

**a generic template for how to do some activities**, consists of:

- Information on how to act and/or perceive (knowledge, data structures, models)

- Computational process by which it achieves the activity (algorithm)

<img src="/Users/dahao/pmlb/robotics/COP518-Robotics-Notes/figures/02-schema-theory.png" alt="image-20200128212146527" style="zoom:40%;" />

<img src="/Users/dahao/pmlb/robotics/COP518-Robotics-Notes/figures/02-schema-example.png" alt="image-20200128215610865" style="zoom:50%;" />





### Emergent Behaviour, why? 

emergence is a property of a collection of interacting components (here, behaviors)

#### Why

- Complexity of the world in which the robot resides
- Complexity of perceiving that world
- Complexity of interactions of agents and the world



### Behaviour Coordination Strategies

#### Competitive

- Fixed prioritization

  <img src="/Users/dahao/pmlb/robotics/COP518-Robotics-Notes/figures/02-prioritization.png" alt="image-20200128215315745" style="zoom: 33%;" />

- Action selection

  <img src="/Users/dahao/pmlb/robotics/COP518-Robotics-Notes/figures/02-selection.png" alt="image-20200128215420226" style="zoom:33%;" />

- Vote generation

  <img src="/Users/dahao/pmlb/robotics/COP518-Robotics-Notes/figures/02-vote.png" alt="image-20200128215515585" style="zoom:33%;" />



#### Cooperative

- Vector addition using potential fields

  <img src="/Users/dahao/pmlb/robotics/COP518-Robotics-Notes/figures/02-vector.png" alt="image-20200128215730104" style="zoom:33%;" />



### Finite State Acceptor Diagrams

<img src="/Users/dahao/pmlb/robotics/COP518-Robotics-Notes/figures/02-fsa.png" alt="image-20200128220444591" style="zoom:33%;" />

<img src="/Users/dahao/pmlb/robotics/COP518-Robotics-Notes/figures/02-fsa-example.png" alt="image-20200128220511107" style="zoom:50%;" />



<img src="/Users/dahao/pmlb/robotics/COP518-Robotics-Notes/figures/02-fsa-cola.png" alt="image-20200128220549087" style="zoom:50%;" />

<img src="/Users/dahao/pmlb/robotics/COP518-Robotics-Notes/figures/02-fsa-cola-table.png" alt="image-20200128220610980" style="zoom:50%;" />



### Representative Reactive/Behavior-Based Architectures

#### Subsumption

Task: recycling coca-cola cans

Simplification:

- only coca-cola cans are red objects

- Only trash bin is blue object in the environment

<img src="/Users/dahao/pmlb/robotics/COP518-Robotics-Notes/figures/02-subsumption.png" alt="image-20200128215944624" style="zoom:50%;" />



##### Strengths:

- Hardware retargetability: Subsumption can compile down directly onto programmable-array logic circuitry

- Support for parallelism: Each behavioral layer can run independently and asynchronously



##### Null (not strength/not weakness):

- Robustness: Can be successfully engineered into system but is often hard-wired and hard to implement

- Timeliness for development: Some support tools exist, but significant learning curve exists



##### Weaknesses:

- Run time flexibility: priority-based coordination mechanism, ad hoc aspect of behavior generation, and hard-wired aspects limit adaptation of system

- Support for modularity: behavioral reuse is not widely done in practice



#### Motor Schemas

- Behavioral responses are all represented as vectors generated using a potential fields approach

- Coordination is achieved by vector addition



### Potential field techniques



### Common fields in behaviours

<img src="/Users/dahao/pmlb/robotics/COP518-Robotics-Notes/figures/03-potential-fields.png" alt="image-20200128221257123" style="zoom:50%;" />

a: uniform   b: perpendicular   

c: attraction   d: repulsion  e: tangential



#### Advantages

- Easy to visualize

- Easy to build up software libraries

- Fields can be parameterized

- Combination mechanism is fixed, tweaked with gains



#### Disadvantages

- Local minima problem (sum to magnitude=0)

- Jerky motion 



### Steps in Designing a Reactive Behavioural System

<img src="/Users/dahao/pmlb/robotics/COP518-Robotics-Notes/figures/03-steps.png" alt="image-20200128230308282" style="zoom:50%;" />



### How to represent a behaviour

