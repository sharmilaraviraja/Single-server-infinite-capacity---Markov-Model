# Single server with infinite capacity (M/M/1):(oo/FIFO)
Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival of materials follow poisson process with the mean interval time 12 seconds, serivice time of lathe machine follows exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.

Software required :
Visual components and Python

## Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.
This is a queuing model in which the arrival is Marcovian and departure distribution is also Marcovian,number of server is one and size of the queue is also Marcovian,no.of server is one and size of the queue is infinite and service discipline is 1st come 1st serve(FCFS) and the calling source is also finite.

## Procedure :

## Program
```
# M/M/1 Queue Model

# Given data
arrival_interval = 12      # seconds
service_time_lathe = 1     # seconds
service_time_robot = 7     # seconds

# Arrival rate (λ)
lam = 1 / arrival_interval

# Total service time
service_time = service_time_lathe + service_time_robot

# Service rate (μ)
mu = 1 / service_time

# Utilization factor
rho = lam / mu

# Average number in system
Ls = rho / (1 - rho)

# Average number in queue
Lq = rho**2 / (1 - rho)

# Average waiting time in system
Ws = Ls / lam

# Average waiting time in queue
Wq = Lq / lam

print("Arrival Rate (λ) =", round(lam, 4), "per second")
print("Service Rate (μ) =", round(mu, 4), "per second")
print("Utilization Factor (ρ) =", round(rho, 4))

print("\nAverage number of materials in system (Ls) =", round(Ls, 4))
print("Average number of materials in conveyor (Lq) =", round(Lq, 4))

print("\nAverage waiting time in system (Ws) =", round(Ws, 4), "seconds")
print("Average waiting time in conveyor (Wq) =", round(Wq, 4), "seconds")
```
## Output :
<img width="525" height="216" alt="image" src="https://github.com/user-attachments/assets/9bc8cf15-4d95-477e-bd49-6e9ce5eb72d1" />

## Result :
Thus Single-server-infinite-capacity---Markov-Model is executed successfully.

