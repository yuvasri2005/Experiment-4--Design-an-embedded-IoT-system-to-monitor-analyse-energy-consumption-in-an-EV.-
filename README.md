# Experiment-4--Design-an-embedded-IoT-system-to-monitor-analyse-energy-consumption-in-an-EV.

## AIM
To design an embedded IoT system to monitor and analyze energy consumption in an electric vehicle (EV). The system tracks voltage, current, power, and energy consumption and provides insights for efficiency optimization.

 
## THEORY
1. Energy Consumption in EVs
•	Power (W) = Voltage (V) × Current (A)
•	Energy (kWh) = Power × Time
•	Battery efficiency = (Energy used / Battery capacity) × 100
2. IoT-Based Monitoring Without Cloud
Instead of using ThingSpeak, this experiment simulates real-time sensor data using MATLAB and analyzes power trends locally.
 
 ## PROCEDURE
🔹 Step 1: Initialize System Parameters
•	Define simulation duration and sensor data range.
•	Simulate voltage and current variations in an EV.
🔹 Step 2: Compute Power and Energy Usage
•	Compute power consumption at each time step.
•	Integrate power over time to calculate total energy consumption.
🔹 Step 3: Analyze and Plot Data
•	Calculate efficiency based on battery capacity.
•	Plot graphs for power and energy consumption trends.
 
## MATLAB CODE (WITHOUT THINGSPEAK)

 
## MATLAB OUTPUT

 
  
## CONCLUSION
This experiment demonstrated an embedded MATLAB system for analyzing EV energy consumption. It helps optimize battery usage and improve vehicle efficiency.

