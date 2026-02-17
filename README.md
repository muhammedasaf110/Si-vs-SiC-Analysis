Case 1: silicon (Si) baseline analysis

In this phase, the power stage utilizes an infineon SPA11N60C3 MOSFET to represent a realistic silicon-based scenario.

Simulation configuration

    Input voltage: 400V

    Switching frequency: 20 kHz (Ts​=50μs)

    Active switch: infineon SPA11N60C3 (650V, 340mΩ)

    Fast recovery diode: VS-E5TH1506

Performance data

Steady-state measurement directives were extracted from the SPICE error log:

    Input power (Pin​): 2179.71 W

    Output power (Pout​): 2150.36 W

    System efficiency: 98.65%

Thermal limitations

<img width="317" height="168" alt="image" src="https://github.com/user-attachments/assets/03f60b6e-d420-4691-8bd0-a31decc54a62" />


    Steady-state loss: the MOSFET requires ~28W of heat rejection, necessitating a physical heatsink at minimum.

    Startup transients: during the initial startup (0ms to 10ms), power spikes exceeded 5.4 kW.

Physical limitations

The 20 kHz silicon architecture creates significant mechanical and spatial bottlenecks:

    Inductor volume: to maintain a stable output at 20 kHz, a large 150µH inductor (L1) is required.

    Weight: high-current SMT magnetic components add substantial mass to the PCB.

    Reliability: these heavy components are susceptible to vibration-induced fatigue and mechanical failure in automotive environments.

Conclusion

By using SiC technology, we can achieve faster transition times. Although higher switching frequencies usually reduce efficiency, the fast transition time of silicon carbide more than makes up for this. This shift to higher switching frequencies allows us to use smaller inductors, thereby making our solution more space-efficient and power-dense.
