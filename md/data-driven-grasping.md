## Data-Driven Grasp Synthesis - A Survey

### Reminders
- dexterous $=$ skillful (esp. with hands) -- e.g. being able to move the pen around while it is grasped
- wrench $=$ noncontact forces and moments applied to the object
- force closure $\implies$ grasp can be maintained in the face of any object wrench -- is aided by friction (c.f. form closure means no movement at all) 

### Overview
- Aproaches divided into grasps of **known**, **familiar** and **unknown** objects
- *grasp synthesis* $=$ "problem of finding a grasp configuration that satisfies a set of criteria relevant for the grasping task"
1. Analytic
    - constrained optimization problem over some of the following criteria on force closure grasps
        - *dexterity*, *equilibrium*, *stability* or certain *dynamics*

2. Empirical (also called data-driven, comparative, knowledge-based)
    - sampling grasp candidates and ranking them according to a specific metric
    - usually parametrised by: the grasping point on the object, approach vector towards the grasping point, wrist orientation and initial finger configuration

### Key ingredients
#### Known objects
- Focus on object recognition and pose estimation

#### Familiar objects
- Use similarity matching to a set of known objects

#### Unknown objects
- Focus on extracting features indicative of good grasps

### Comments