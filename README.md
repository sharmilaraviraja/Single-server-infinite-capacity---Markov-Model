# Single server with infinite capacity (M/M/1):(oo/FIFO)
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

