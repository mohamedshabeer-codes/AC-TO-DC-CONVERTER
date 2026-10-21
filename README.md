## 📌 PCB Functionality & Bill of Materials (BOM)

### ⚡ Circuit Functionality
* **AC Input (`J1`):** Accepts a low-voltage AC input signal[cite: 1].
* **Full-Wave Rectification (`D1`–`D4`):** Uses a bridge rectifier made of four `1N4007` diodes to convert the incoming AC waveform into pulsating DC[cite: 1].
* **Filtering & Smoothing (`C1`):** A `1000µF` electrolytic capacitor smooths out the rectified voltage ripple[cite: 1].
* **Bleeder Discharge (`R1`):** A `10kΩ` resistor safely discharges the filter capacitor when the circuit is powered down[cite: 1].
* **Power Indicator (`R2`, `D5`):** A red LED paired with a `2.2kΩ` current-limiting resistor lights up to indicate active DC output[cite: 1].
* **DC Output (`J2`):** Delivers the smoothed DC voltage via a 2-pin screw terminal[cite: 1].

---

## ⚡ Operating Input & Output Voltage Specs

* **Input Voltage:** **12V AC**
* **Peak Output Voltage (V_peak):** approx. **15.5V DC** (Unloaded, calculated as 12V × 1.414 - 1.4V drop across the bridge rectifier diodes)
* **Nominal / Filtered DC Output:** approx. **12V – 14V DC** under typical light-to-moderate loads, smoothed by the 1000µF filter capacitor[cite: 1].
* **Maximum Current Rating:** Up to **1A** continuous, limited by the current handling capacity of the 1N4007 rectifier diodes[cite: 1].

### 🛠️ Bill of Materials (BOM)

| Designator | Quantity | Component / Value | Footprint / Package | Description |
| :--- | :---: | :--- | :--- | :--- |
| **J1** | 1 | Screw Terminal (1x02) | 2-pin 5.08mm Screw Terminal | AC Voltage Input[cite: 1] |
| **J2** | 1 | Screw Terminal (1x02) | 2-pin 5.08mm Screw Terminal | DC Voltage Output[cite: 1] |
| **D1, D2, D3, D4** | 4 | 1N4007 | DO-41 Through-Hole | Rectifier Diodes (1A / 1000V)[cite: 1] |
| **C1** | 1 | 1000µF / 25V (or higher) | Radial Electrolytic | Filter Capacitor[cite: 1] |
| **R1** | 1 | 10kΩ | Axial Through-Hole | Bleeder Resistor[cite: 1] |
| **R2** | 1 | 2.2kΩ | Axial Through-Hole | Current Limiting Resistor for LED[cite: 1] |
| **D5** | 1 | 5mm LED (Red) | 5mm Radial LED | Power Indicator[cite: 1] |

---

<p align="left">
  <img src="https://img.shields.io/badge/Made%20with-KiCad-1951be?style=for-the-badge&logo=kicad&logoColor=white" alt="Made with KiCad">
</p>
