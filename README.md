#AEP Arrivals Simulation (Monte Carlo)
Discrete-event simulation project modeling aircraft arrivals and landings at Buenos Aires' Aeroparque Jorge Newbery (AEP) under demand uncertainty and unexpected disruptions.

##Overview
This project simulates the approach and landing process at AEP, an airport whose daily operation handles a large volume of flights and is highly sensitive to air traffic congestion during peak hours and adverse weather conditions. These factors introduce uncertainty into the approach process, creating the risk of delays, service saturation, and diversions to alternative airports such as Montevideo.

The simulation models each aircraft's approach starting when it appears on radar 100 nautical miles from the airport, with speed adjusted according to distance to the runway and separation from the preceding aircraft (a minimum 4-minute separation is enforced). If an aircraft cannot maintain the minimum required speed, it must leave the queue: it attempts to re-insert itself if a gap of at least 10 minutes is available, or diverts to Montevideo otherwise. The model also incorporates special events such as changes in the arrival rate (λ), point interruptions in approaches, and sudden storms or AEP closures. The system is simulated minute by minute using a Monte Carlo approach with arrivals modeled as a Poisson process, capturing realistic congestion and delay dynamics.

The simulation was used to compare a baseline scenario against more adverse cases involving interruptions and storms, measuring performance indicators such as landings, delays, congestion, and diversions. Results revealed a clear trade-off between delays and diversions: at low arrival rates the airport operates stably with nearly all flights landing without major issues; at intermediate rates, delays and diversions increase, revealing the system's vulnerability; and at high rates, saturation forces most flights to divert, which artificially lowers average delay while sharply increasing overall inefficiency.

Two alternative operating policies were also evaluated. The first reduced diversions to Montevideo and increased the landing rate, at the cost of higher congestion and delay at high arrival rates. The second showed better performance in terms of congestion and delay at higher arrival rates. Together, these results reinforced the model's usefulness for designing operational improvements, showing that relatively simple adjustments to approach management can translate into substantial gains in system performance.

##Academic Context
This project was developed as part of a coursework assignment at Universidad Torcuato Di Tella.
