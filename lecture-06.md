## Lecture 6: Topological Path Planning

### Spatial Memory

A robot’s world representation and how it is maintained over time.



### Route, or Qualitative Navigation

- *Relational*
  - spatial memory is a **relational graph**, also known as a topological map
  - use graph theory to plan paths

- *Associative*
  - spatial memory is a series of **remembered viewpoints**, where each viewpoint is labeled with a location
  - good for retracing steps
  - Advantages:
    - Tight coupling of sensing to homing
    - Robot does not need to explicitly recognize what a landmark is
    - Enables robots to build up maps as it explores
  - Disadvantages:
    - Require massive storage
    - Brittle in presence of dynamic world when landmarks may be occluded or change



### Dijkstra's algorithm