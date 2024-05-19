# Consensus Filters for Sensor Networks

## Description

**Consensus Filters for Sensor Networks** is a project focused on implementing and analyzing consensus algorithms in a network of 50 sensor nodes. Each node makes independent measurements and communicates with its neighbors to reach a consensus on the estimated value. The project involves both static and dynamic sensor network configurations, utilizing Max-Degree and Metropolis weights to achieve consensus. The primary objective is to minimize the mean-square error between the estimated values and the ground truth, which is set at 50.

### Features

- **Sensor Network Configuration**: A network of 50 sensor nodes distributed over a specified area with adjustable active ranges to define the number of neighbors.
- **Noise Distribution**: Each sensor node generates a measurement `yi = 50 + Noise`, where Noise is Gaussian noise with a mean of 0.
- **Consensus Algorithms**:
  - **Max-Degree Weights**
  - **Metropolis Weights**
- **Network Types**:
  - **Static Sensor Network**
  - **Dynamic Sensor Network**

### Implementation Details

- **Programming Language**: Python
- **Libraries**: NumPy for numerical operations, Matplotlib for plotting, and NetworkX for handling graph-based sensor networks.

### How It Works

1. **Initialization**:
   - Nodes are initialized with random positions and assigned neighbors based on the specified active range.
   - Each node generates a measurement `yi = 50 + Noise`.

2. **Consensus Algorithm**:
   - Implement Max-Degree and Metropolis weights for both static and dynamic sensor networks.
   - Nodes communicate with their neighbors and iteratively update their estimates based on the consensus algorithm.

3. **Error Calculation and Plotting**:
   - Calculate the mean-square error between the estimated values and the ground truth.
   - Plot the required graphs for both static and dynamic sensor networks.

### Results

The following visualizations are generated to analyze the performance of the consensus algorithms:

#### Static Sensor Network

![Mean-Square Error (Convergence)](images/mse_convergence.png)
*Mean-Square Error between the estimated values and the ground truth.*

![Node Degree Error](images/node_degree_error.png)
*Mean-Square Error of the node with the largest number of neighbors and the node with the smallest number of neighbors.*

![Initial vs Final Estimates](images/initial_vs_final.png)
*Initial measurements versus the final estimates of all sensor nodes.*

#### Dynamic Sensor Network

![Dynamic Mean-Square Error (Convergence)](images/dynamic_mse_convergence.png)
*Mean-Square Error between the estimated values and the ground truth in a dynamic network.*

### Conclusion

**Consensus Filters for Sensor Networks** demonstrates the effectiveness of consensus algorithms in both static and dynamic sensor networks. By analyzing the mean-square error and node-specific errors, this project provides insights into the performance and robustness of different consensus weighting schemes.