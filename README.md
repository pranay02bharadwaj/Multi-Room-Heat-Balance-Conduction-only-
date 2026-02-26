Multi-Room Heat Balance (Conduction Only) – MATLAB Implementation

1. Overview
This project presents a MATLAB-based implementation of a **multi-room heat balance model** considering **conduction as the only mode of heat transfer**. The model analyzes steady-state heat transfer between interconnected rooms and the surrounding ambient environment using linear energy balance equations. A graphical representation of room-wise temperature distribution is generated for interpretation.

2. Objective
The objectives of this project are:
- To model heat transfer between multiple rooms using conduction
- To formulate linear energy balance equations for each room
- To develop a matrix-based mathematical model
- To compute steady-state room temperatures using MATLAB
- To visualize temperature variation across rooms

3. Mathematical Model
At steady state, the heat balance equation for a room is expressed as:

\[
\sum Q_{in} - \sum Q_{out} + Q_{gen} = 0
\]

Using thermal resistance and conductance concepts, the governing equations can be written in matrix form as:

\[
[A][T] = [B]
\]

Where:
- \( A \) is the coefficient matrix containing thermal conductances  
- \( T \) is the vector of unknown room temperatures  
- \( B \) represents ambient temperature effects and internal heat generation  

The system is solved numerically to obtain the steady-state temperature of each room.

4. Project Structure and File Description
The project follows a simple and organized structure:

Multi_Room_Heat_Balance/
│
├── multi_room_heat_balance.m  
│   - Defines thermal resistances and conductances  
│   - Constructs energy balance matrices  
│   - Solves the system of linear equations  
│   - Generates temperature distribution graph  
│
├── README.md  
│   - Contains theoretical background, modeling, and result interpretation  

5. Input Data

5.1 Thermal Resistance Parameters
- Resistance between adjacent rooms:  
  \( R_1 = 0.1 \ \text{K/W} \)
- Resistance between room and ambient:  
  \( R_2 = 0.48 \ \text{K/W} \)

5.2 Boundary Conditions
- Ambient temperature:  
  \( T_{amb} = 35^\circ C \)
- Internal heat generation in top room:  
  \( Q_{gen} = 50 \ \text{W} \)

6. MATLAB Implementation
The MATLAB code performs the following steps:
1. Initializes thermal resistances and ambient conditions
2. Converts resistances to conductances
3. Formulates linear energy balance equations in matrix form
4. Solves the system using MATLAB’s backslash operator (\)
5. Plots room temperature versus room number

7. Output and Visualization
The output is a temperature distribution plot showing:
- Steady-state temperature of each room
- A gradual temperature increase from lower to upper rooms
- The effect of internal heat generation on the top room

8. Key Observations
- The ground room exhibits the lowest temperature due to ambient heat loss
- The top room shows the highest temperature because of internal heat generation
- A smooth temperature gradient confirms conduction-dominated heat transfer
- The linear model accurately captures inter-room thermal interaction

9. Applications
- Building thermal analysis  
- HVAC system design (preliminary analysis)  
- Energy-efficient building studies  
- Academic heat transfer modeling  

10. Conclusion
This project demonstrates the application of steady-state energy balance equations to analyze heat transfer in a multi-room system considering conduction only. The MATLAB-based matrix solution provides an efficient and scalable approach for predicting room temperatures. The results highlight the importance of inter-room heat transfer and internal heat generation in determining temperature distribution, making the model useful for both academic and practical engineering applications.
