Case 1: Silicon baseline

For this simulation, the circuit uses an Infineon SPA11N60C3 CoolMOS to represent a realistic silicon-based scenario.

Simulation config:

    Input voltage: 400V

    Switching frequency: 20 kHz (Ts = 50µs)

    Active switch: Infineon SPA11N60C3 (650V, 340mΩ)

    Fast recovery diode: VS-E5TH1506

    Measurement window: 30ms to 40ms (steady-state)

Performance Data

Using steady-state measurement directives, the following results were extracted from the SPICE Error Log:

Thermal limitation:

<img width="317" height="172" alt="image" src="https://github.com/user-attachments/assets/6390c8a9-ca3a-48fc-ae6e-f440dabc866a" />

~28 watts of heat rejection requires a heatsink and airflow. 

Furthermore, during the initial startup transient (0ms to 10ms), power spikes reached over 5.4 kW, leading to a much higher average dissipation of 125.36 W over the full 40ms window.

Physical limitation:

The primary drawback of this 20 kHz silicon architecture is size.

    To maintain stable output at 20 kHz, a large 150µH Inductor (L1) is required.

    Using high-current SMT components introduces significant weight to the PCB.

    Heavy magnetic components are susceptible to vibration damage in automotive environments.

Conclusion:
By using SiC technology, we can achieve faster transition times. Although higher switching frequencies usually reduce efficency, the fast transition time of silicon-carbide more than makes up for this. This shift to higher switching frequencies allows us to use smaller inductors, thereby making our solution more space-efficient and power-dense.
