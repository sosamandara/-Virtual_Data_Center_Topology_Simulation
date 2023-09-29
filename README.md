# -Virtual_Data_Center_Topology_Simulation

*Overview*
This readme provides an overview of a simulation project that focuses on evaluating the performance of two virtual data center topologies: Fat-Tree and Jellyfish. The simulation assesses the response time and job running cost as functions of the number of servers used to process a generic job in these topologies. This project employs Python with the Networkx module to conduct the simulation.

*Simulation Steps*
1. *Building Virtual Data Center Topology*
*Fat-Tree Topology*
- Calculates the number of core switches, aggregator switches, edge switches, and servers needed.
- Constructs an empty graph and populates it with different types of nodes, including core, aggregator, edge switches, and servers.
- Establishes connections between switches following the Fat-Tree structure, connecting edge switches to servers.

  
*Jellyfish Topology*

- Creates a topology with the same number of switches as Fat-Tree but with a different interconnect scheme.
- Uses the r-regular graph function to ensure each switch has a specific degree (r connections).
- Adds servers to each switch.

  
2. *Simulating Response Time (R) and Job Running Cost (S)*
   
*Simulation Setup*
- Randomly selects a server (A) from the virtual network.
- Identifies the N nearest servers to A using Dijkstra's algorithm.
- Simulates task completion time for each neighbor server based on an exponential distribution.
- Simulates the output size for each neighbor server.
- Calculates the Round Trip Time (RTT) between A and each neighbor.
- Computes the average throughput for each neighbor.
- Determines the time it takes for each neighbor to receive input from A and send output back to A.

*Response Time and Job Running Cost*
- Computes the response time (R) as the sum of task completion time, RTT, and input/output transfer time.
- Calculates the job running cost (S) as the sum of response times for all neighbors.

  
3. *Repeating the Simulation*
- Repeats the entire simulation process 100 times for N values ranging from 1 to 10,000.
- Calculates the mean response time (E[R]) and job running cost (S) for each N.
- Normalizes the results over the response time and job running cost when only server A is used (Rbase and Sbase).

  
*Results and Analysis*
The readme includes figures illustrating the average expected response time and job running cost for both Fat-Tree and Jellyfish topologies as a function of the number of servers used to split the job. Key findings are highlighted, such as the optimal number of servers that minimize job running cost and the impact of adding more servers on performance.

*Conclusion*

The readme concludes by emphasizing the importance of performance studies to determine the ideal number of servers and avoid network overload in data center topologies. It summarizes the project's key insights and encourages further exploration of virtual data center topologies and their performance characteristics.
