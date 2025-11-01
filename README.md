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

clear; clc; close all;

% Simulation Parameters timeDuration = 60;

% Simulation time in minutes timeStep = 1;

% Time step in minutes

% Simulated voltage and current data (Example: EV under different conditions) 

voltageData = 360 + 10 * randn(1, timeDuration);

% Voltage fluctuates around 360V currentData = 50 + 5 * randn(1, timeDuration);

% Current fluctuates around 50A


% Initialize arrays for power and energy consumption 

powerData = zeros(1, timeDuration); 
energyData = zeros(1, timeDuration);

% Battery capacity assumption

batteryCapacity = 40 * 1000;

% 40 kWh converted to Wh

% Energy analysis loop

for t = 1:timeDuration powerData(t) = voltageData(t) * currentData(t);

% P = V * I (Watt) energyData(t) = powerData(t) * (timeStep / 60);

% Energy in kWh per minute end

% Total Energy Consumption

totalEnergy = sum(energyData);

% Total energy used in kWh

% Efficiency Calculation 

efficiency = (totalEnergy / batteryCapacity) * 100;

% Efficiency as a percentage

% Display results disp(['Total Energy Used: ', num2str(totalEnergy), ' kWh']); 

disp(['Estimated Efficiency: ', num2str(efficiency), ' %']);

% Plot Energy Consumption Over Time

figure; 

subplot(2,1,1);

plot(1:timeDuration, powerData, 'b', 'LineWidth', 1.5);

xlabel('Time (minutes)');

ylabel('Power (W)'); 

title('Power Consumption Over Time');

grid on;

subplot(2,1,2); 

plot(1:timeDuration, cumsum(energyData), 'r', 'LineWidth', 1.5);

xlabel('Time (minutes)'); 

ylabel('Cumulative Energy (kWh)');

title('Total Energy Consumption Over Time'); 

grid on;

 
## MATLAB OUTPUT

<img width="699" height="625" alt="image" src="https://github.com/user-attachments/assets/9fb6b07b-cb18-4ce0-a43b-ca83fbeb6293" />


 
  
## CONCLUSION
This experiment demonstrated an embedded MATLAB system for analyzing EV energy consumption. It helps optimize battery usage and improve vehicle efficiency.

