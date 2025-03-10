
# Vehicle Inspection and Emissions Testing Process Simulation

This repository contains an AnyLogic simulation model of a **Vehicle Inspection and Emissions Testing Process**. The simulation replicates a real-world process where personal vehicles undergo a series of inspections and emissions testing at a facility, with detailed resource allocation and performance monitoring.

## Project Overview

The simulation models a vehicle inspection facility that processes **75 vehicles per day** during an **8-hour workday**. The goal of the simulation is to monitor key performance metrics such as resource utilization, throughput time, and waiting times for the inspection process.

### Key Features:
- Models the step-by-step process of vehicle inspection, including:
  - **Check-in** at the reception.
  - Calling vehicle insurance.
  - Moving vehicles to inspection bases.
  - Performing inspections at different bases.
  - Recording results.
- Incorporates **randomized delays** based on statistical distributions (e.g., uniform and triangular distributions).
- Tracks **resource utilization** for receptionists and inspectors.
- Outputs key performance indicators such as:
  - Total completed vehicle inspections.
  - Mean utilization of stations and resources.
  - Throughput and waiting times for each station.

---

## Process Details

### Input Parameters:
- **Arrival rate**: 9 vehicles per hour.
- **Operating hours**: 8:00 AM to 5:00 PM (Monday to Friday, with a 1-hour lunch break).
- **Inspection lanes**: 3 dedicated lanes (Lane 1, Lane 2, Lane 3).

### Process Flow:
The vehicle inspection process follows the sequence below:

| **Activity**                | **Duration (Minutes)**      | **Resource Allocated**   |
|-----------------------------|-----------------------------|--------------------------|
| Check-in                   | Uniform(0.1, 2)            | Receptionist             |
| Call insurance             | Triangular(20, 30, 60)     | Receptionist             |
| Move vehicle               | Triangular(2, 5, 20)       | Inspector at Base 2      |
| Inspection at Base 2       | Uniform(4, 10)             | Inspector at Base 2      |
| Inspection at Base 3       | Uniform(1, 2)              | Inspector at Base 3      |
| Inspection at Base 4       | Uniform(4, 12)             | Inspector at Base 4      |
| Recording results          | Fixed(1)                   | Receptionist             |

### Probabilities:
- **Inspection lane selection**:
  - Lane 1: 45%
  - Lane 2: 45%
  - Lane 3: 10%
- **Inspection outcomes**:
  - Vehicles failed at Base 2 (first inspection): 15.23%
  - Vehicles failed at Base 3 (second inspection): 1.75%
  - Vehicles passed at Base 4 (third inspection): 92.37%

---

## Resources Involved

- **Receptionist**: 1 receptionist handles check-in, insurance calls, and recording results.
- **Inspectors**:
  - 3 inspectors are assigned to dedicated bases (Base 2, Base 3, and Base 4).
- **Working Schedule**:
  - Monday to Friday
  - 8:00 AM to 5:00 PM
  - 1-hour break at 12:00 PM.

---

## Simulation Results

The simulation tracks the following key performance indicators (KPIs):
1. **Total completed vehicle inspections**.
2. **Mean utilization of stations**:
   - Check-in, Insurance Call, and Inspection Bases.
3. **Mean utilization of resources**:
   - Receptionist and Inspectors.
4. **Throughput time**:
   - Total time for vehicles to pass through all inspections (Base 2 → Base 4).
5. **Waiting time**:
   - Time vehicles spend waiting at each station.

---

## How to Run the Simulation

1. Install [AnyLogic](https://www.anylogic.com/) simulation software.
2. Download or clone this repository:
   ```bash
   https://github.com/seyedmohammadrezaayazi/THE-VEHICLE-INSPECTION
   ```
3. Open the `.alp` file in AnyLogic.
4. Configure the input parameters if needed (e.g., arrival rate, resource capacity).
5. Run the simulation and monitor the output metrics in the dashboard.

---

## Files in This Repository

- **`OM assignment - additional data.pdf`**: Detailed description of the inspection process and parameters.
- **Simulation Model Files**: The AnyLogic project file (`.alp`) and supporting files.
- **README.md**: This file provides an overview of the project.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

## Author

  Seyed Mohammadreza Ayazi


If you have any questions or suggestions, feel free to open an issue or contact me.


