# Banker's Algorithm Simulator

A web-based interactive simulator for the Banker's Algorithm, a deadlock avoidance algorithm used in operating systems to safely allocate resources to processes.

## About

The Banker's Algorithm is a resource allocation and deadlock avoidance algorithm that tests for safety by simulating the allocation of predetermined maximum possible amounts of all resources, and then makes an "s-state" check to test for possible activities before deciding whether allocation should be allowed to continue.

## Features

- **Interactive Input**: Enter the number of processes and resource types
- **Dynamic Tables**: Automatically generate allocation, maximum, and resource tables
- **Need Calculation**: Calculate the need matrix (Maximum - Allocation)
- **Available Resources**: Calculate available resources
- **Safe Sequence Generation**: Find a safe sequence for process execution
- **Resource Request Simulation**: Simulate resource requests and check if they lead to a safe state
- **Visual Feedback**: Color-coded tables and step-by-step execution display

## How to Use

1. **Open the Application**: Open `index.html` in your web browser or visit the [live demo](https://groot-077.github.io/Bankers-Algorithm/)

2. **Enter Initial Values**:
   - Enter the number of processes (e.g., 5)
   - Enter the number of resource types (e.g., 3)
   - Click "Create All Tables"

3. **Fill in the Tables**:
   - **Resource Table**: Enter the total instances of each resource type
   - **Allocation Table**: Enter the current allocation of resources to each process
   - **Maximum Table**: Enter the maximum resource needs for each process

4. **Calculate Need Matrix**:
   - Click "Find need" to calculate the Need matrix (Maximum - Allocation)

5. **Calculate Available Resources**:
   - Click "Find available" to calculate the available resources

6. **Find Safe Sequence**:
   - Click "Find Safe Sequence" to determine if a safe sequence exists
   - The algorithm will display the safe sequence and step-by-step execution

7. **Simulate Resource Requests** (Optional):
   - Click "Make a Resource Request"
   - Enter the process number that wants to make a request
   - Enter the requested resources
   - Click "Check Safe state" to see if granting the request maintains system safety

8. **Reset**: Click "Reset" to start over with new values

## Example

**Initial Setup**:
- Processes: 5
- Resource Types: 3
- Resources: A=10, B=5, C=7

**Allocation Matrix**:
```
P0: 0, 1, 0
P1: 2, 0, 0
P2: 3, 0, 2
P3: 2, 1, 1
P4: 0, 0, 2
```

**Maximum Matrix**:
```
P0: 7, 5, 3
P1: 3, 2, 2
P2: 9, 0, 2
P3: 2, 2, 2
P4: 4, 3, 3
```

The simulator will calculate the Need matrix, Available resources, and determine if a safe sequence exists.

## Technology Stack

- **HTML5**: Structure and layout
- **CSS3**: Styling and visual design
- **JavaScript**: Algorithm implementation and DOM manipulation

## File Structure

```
Bankers-Algorithm/
├── index.html                 # Root redirect page
├── README.md                  # Documentation
└── Operating System/
    ├── index.html            # Main application page
    ├── code.js               # JavaScript implementation
    └── style.css             # Styling
```

## Algorithm Overview

The Banker's Algorithm uses the following key concepts:

- **Available**: A vector of length m indicating the number of available resources of each type
- **Maximum**: An n × m matrix defining the maximum demand of each process
- **Allocation**: An n × m matrix defining the number of resources of each type currently allocated to each process
- **Need**: An n × m matrix indicating the remaining resource need of each process (Need = Maximum - Allocation)

The algorithm checks if there exists a safe sequence of process execution that avoids deadlock.

## License

This project is open source and available under the MIT License.

## Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

## Author

Created by [Groot-077](https://github.com/Groot-077)