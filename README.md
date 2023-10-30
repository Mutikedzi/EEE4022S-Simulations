# EEE4022S-Simulations

To get the combined results, run the corresponding codes first(arrival splitting and service splitting) for each parameter being changed. 
The codes are named according to the parameters being changed. For example, "Arrival_bbu" represents a code for arrival splitting when the bbu is changing, "Service_bbu" represents a code for service splitting when bbu is changing, and so on.

# Running Codes

New Call Arrival Rate  Ploting 
Run "Arrival_new_call.mlx" and "Service_new_call.mlx" first on LiveScript and then run the following code on the command window:

To get Probabilities:

figure; 
plot(ar_new_values, PB_values_arrival, '-ob', 'DisplayName', 'PB_A'); 
hold on; 
plot(ar_new_values, PD_values_arrival, '-xb', 'DisplayName', 'PD_A'); 
plot(ar_new_values, PB_values_service, '-oc', 'DisplayName', 'PB_S'); 
plot(ar_new_values, PD_values_service, '-xc', 'DisplayName', 'PD_S'); 
xlabel('New call arrival rate'); 
ylabel('Probability'); 
title('Blocking and Dropping Probabilities'); 
grid on; 
ylim([0, 1]); 
legend('Location', 'NorthWest'); 
 

To get Utilization:
 
figure; 
plot(ar_new_values, utilization_values_service, '-or', 'DisplayName', 'U_S'); 
hold on; 
plot(ar_new_values, utilization_values_arrival, '-ob', 'DisplayName', 'U_A'); 
xlabel('New call arrival rate'); 
ylabel('Normalized utilization'); 
title('Network Utilization '); 
grid on; 
ylim([0, 1]); 
legend('Location', 'NorthWest'); 

  

#Effect of changing bandwidth
Run "Arrival_bbu.mlx" and "Service_bbu.mlx" first on Livescript and then run the following code on the command window:

To get Probabilities:

figure; 
plot(bbu_values, PB_values_arrival_bbu, '-ob', 'DisplayName', 'PB_A'); 
hold on; 
plot(bbu_values, PD_values_arrival_bbu, '-xb', 'DisplayName', 'PD_A'); 
plot(bbu_values, PB_values_service_bbu, '-or', 'DisplayName', 'PB_S'); 
plot(bbu_values, PD_values_service_bbu, '-xr', 'DisplayName', 'PD_A'); 
xlabel('Required bandwidth per call'); 
ylabel('Probability'); 
title('Blocking and Dropping Probability'); 
grid on; 
ylim([0, 1]); 
legend('Location', 'NorthWest'); 
 
 

To get Utilization: 

figure; 
plot(bbu_values, utilization_values_arrival_bbu, '-ob', 'DisplayName', 'U_A'); 
hold on; 
plot(bbu_values, utilization_values_service_bbu, '-or', 'DisplayName', 'U_S'); 
xlabel('Required bbu per call'); 
ylabel('Normalized utilization'); 
title('Network Utilization '); 
grid on; 
ylim([0, 1]); 
legend('Location', 'NorthWest'); 

   

#Effect of Departure rate Ploting 
Run "Arrival_departure.mlx" and "Service_departure.mlx" first on LiveScript and then run the following code on the command window:

To get Probabilities:


figure; 
plot(dr_new_values, PB_values_arrival_changing_dr, '-ob', 'DisplayName', 'PB_A'); 
hold on; 
plot(dr_new_values, PD_values_arrival_changing_dr, '-xb', 'DisplayName', 'PD_A'); 
plot(dr_new_values, PB_values_service_changing_dr, '-or', 'DisplayName', 'PB_S'); 
plot(dr_new_values, PD_values_service_changing_dr, '-xr', 'DisplayName', 'PD_S'); 
xlabel('New call departure rate'); 
ylabel('Probability'); 
title('Blocking and Dropping Probabilities '); 
grid on; 
ylim([0, 1]); 
legend('Location', 'NorthWest'); 


To get Utilization:

figure; 
plot(dr_new_values, utilization_values_arrival_changing_dr, '-ob', 'DisplayName', 'U_A'); 
hold on; 
plot(dr_new_values, utilization_values_service_changing_dr, '-or', 'DisplayName', 'U_S'); 
xlabel('New call departure rate'); 
ylabel('Normalized utilization'); 
title('Network Utilization '); 
grid on; 
ylim([0, 1]); 
legend('Location', 'NorthWest'); 



# Effect of changing Threshold Ploting 
Run "Arrival_threshold1.mlx" and "Service_threshold1.mlx" first on livescript and then run the following code on the command window:


To get Probabilities:
 
figure; 
plot(T1_values, PB_values_arrival_threshold, '-ob', 'DisplayName', 'PB_A'); 
hold on; 
plot(T1_values, PD_values_arrival_threshold, '-xb', 'DisplayName', 'PD_A'); 
plot(T1_values, PB_values_service_threshold, '-or', 'DisplayName', 'PB_S'); 
plot(T1_values, PD_values_service_threshold, '-xr', 'DisplayName', 'PD_S'); 
xlabel('Threshold'); 
ylabel('Probability'); 
title('Blocking and Dropping Probabilities '); 
grid on; 
ylim([0, 1]); 
legend('Location', 'NorthWest'); 

 
To get Utilization:

figure; 
plot(T1_values, utilization_values_threshold, '-ob', 'DisplayName', 'U_A'); 
hold on; 
plot(T1_values, utilization_values_service_threshold, '-or', 'DisplayName', 'U_S'); 
xlabel('Threshold'); 
ylabel('Normalized utilization'); 
title('Network Utilization '); 
grid on; 
ylim([0, 1]); 
legend('Location', 'NorthWest'); 
