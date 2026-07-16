# Simulation Results

This section presents the simulation outcomes of the designed **Variable Gain Amplifier (VGA)**. The circuit was evaluated through pre-layout and post-layout simulations after parasitic RC extraction to observe the effect of layout parasitics on overall circuit performance.

---

# Pre-Layout Simulation

Pre-layout simulations were performed using the schematic-level design before physical layout implementation.

## AC Analysis

The AC analysis was carried out to evaluate the small-signal gain and bandwidth characteristics of the amplifier for different control voltages.

<p align="center">
<img src="../docs/images/pre_layout_ac.png">
</p>

---

## Transient Analysis

Transient simulations were performed to verify the amplifier's time-domain response under sinusoidal excitation.

<p align="center">
<img src="../docs/images/pre_layout_trans.png">
</p>

---

# Post-Layout Simulation

Following layout completion, DRC verification, LVS verification, and RC extraction, post-layout simulations were performed using the extracted netlist.

## AC Analysis

The extracted parasitic resistances and capacitances were included during simulation to evaluate the practical performance of the circuit.

<p align="center">
<img src="../docs/images/post_layout_ac.png">
</p>

---

# Performance Comparison

The table below compares the pre-layout and post-layout performance for a representative control voltage (**Vcont = 602.273 mV**).

| Parameter | Pre-Layout | Post-Layout |
|-----------|-----------:|------------:|
| Gain | **2.3718 V/V** | **2.379 V/V** |
| Gain (dB) | **7.501 dB** | **7.531 dB** |
| Power Consumption | **495.179 μW** | **459.532 μW** |
| Maximum Bandwidth | **4.904 GHz** | **5.109 GHz** |

---

# Monte Carlo Analysis

Monte Carlo analysis was performed to evaluate the robustness of the amplifier against process variations and device mismatches.

<p align="center">
<img src="../docs/images/Monte_carlo.png">
</p>

The statistical analysis confirms that the amplifier maintains stable gain characteristics under manufacturing process variations, indicating reliable circuit operation.

---

# Observations

- The amplifier successfully completed both pre-layout and post-layout verification.
- Post-layout gain remained nearly identical to the schematic-level design.
- The extracted layout demonstrated a slight improvement in bandwidth.
- Power consumption reduced after post-layout extraction.
- Monte Carlo analysis verified the robustness of the design against process-induced variations.

---

# Summary

| Metric | Final Value |
|---------|------------:|
| Technology | **180 nm CMOS** |
| Supply Voltage | **1.8 V** |
| Maximum Gain | **7.531 dB** |
| Maximum Voltage Gain | **2.379 V/V** |
| Maximum Bandwidth | **5.109 GHz** |
| Post-Layout Power | **459.532 μW** |
| Monte Carlo Analysis | **Completed** |
| DRC | **Passed** |
| LVS | **Passed** |
| RC Extraction | **Completed** |
