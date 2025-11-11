# Lift-scheduling
In high-rise construction projects, inefficient delivery of materials, equipment, and labor can impact the completion time of the project. So, improvement in vertical transportation could save time, facilitate the supply process and reduce costs. The methods introduced for efficiently planning lifts in the construction industry were focused on material transportation and the time of lift activity, which primarily used heuristics and simulations. One of the main challenges that has not been fully addressed in the literature is automatically prioritizing critical activities in the supply process. Other issues include taking into account the night shift and considering the deadline of critical activities. This paper proposes a novel mathematical model to obtain the optimal vertical transportation plan considering night shifts and deadlines of critical activities. To do so, a Mixed-Integer Linear Programming (MILP) is introduced that seeks the best allocation of materials and equipment to a given number of travel rounds of the lift. Also, when the demand exceeds lift capacity, the proposed method allows for efficient prioritization of activities and supplies maximum ordered material with the fewest possible delays. The proposed model, coupled with a novel iterative search algorithm, can achieve the minimum number of travel rounds and the optimum lift planning. Field data from a 22-story construction project is used to test the suggested method. The results demonstrate that the method could effectively minimize delivery times and detect infeasible and undersupplied demands.

# Proposed Lift Scheduling Method

The codes for the proposed method have been uploaded here. Three files are provided to facilitate replication and further use of the model:

1. **MODEL**: Contains the Mixed-Integer Linear Programming (MILP) model of the proposed method.
2. **DATA1**: Input data for scenarios representing typical working days with average workload.
3. **DATA2**: Input data for scenarios representing busy days with heavy schedules.

## Usage

To apply the code to other scenarios, simply replace the data file. The key parameters are defined as follows:

- `Mt`: Total duration of night and day shifts
- `M`: A sufficiently large number
- `Nm`: Number of materials that can be transported
- `Ni`: Number of building floors
- `Nl`: Number of lift travel rounds
- `r`: Time required for the lift to move one floor
- `V`: Overall volumetric capacity of the lift
- `W`: Overall weight capacity of the lift
- `f`: Loading/unloading time per unit of material
- `v`: Volumetric capacity of the lift for each material type
- `w`: Weight capacity of the lift for each material type
- `c`: Lift capacity for each material type
- `S`: Start time of the night shift
- `F`: Start time of the day shift
- `D`: Required quantity of each material per floor
- `e`: Critical delivery time of each material on each floor

This setup allows other researchers to adapt the model to different scenarios by simply modifying the input data file.

