# Inductive-source-degeneration-LNA-design
Design a Inductive source degeneration under UMC 65nm technology

#  LNA Design using UMC 65nm CMOS

##  Overview
This project focuses on the **design, simulation, and analysis of a Low Noise Amplifier (LNA)** using **UMC 65nm CMOS technology** in Cadence Virtuoso. The objective is to achieve proper input matching, gain, noise performance, and linearity for RF applications.

---

##  Course Information
- **Institute**: Indian Institute of Space Science and Technology (IIST), Thiruvananthapuram  
- **Department**: Avionics  
- **Course**: AVM – 862 RF Integrated Circuits  

---

##  Design Specifications

- **Technology**: UMC 65nm CMOS  
- **Center Frequency Options**:
  - 900 MHz  
  - 2.4 GHz  
  - 10.5 GHz  

- **LNA Topologies** (any one):
  - Common Gate (CG)  
  - Resistive Feedback  
  - Common Source with Inductive Degeneration  

---

##  Design Guidelines

- Transistor biasing using **current mirrors** (no voltage sources)  
- On-chip inductors:
  - **Q = 10**
  - Max value = 10 pH  
- On-chip capacitors:
  - Max value = 15 pF  
- Add:
  - **Buffer stage** to drive 50Ω load  
  - **DC blocking capacitors** at input/output  
- Start with:
  - **DC analysis** before RF simulations  

---

##  Simulation Flow

### 1. DC Analysis
- Verify:
  - Bias currents  
  - Node voltages  
  - Transistors in saturation  
  - Parameters like gm, ro  

---

### 2. S-Parameter Analysis

#### Input Matching
- Plot **S11 (log magnitude)**  
- Condition:
  - S11 < -10 dB at operating frequency  
- Determine **input bandwidth**

#### Gain
- Plot **S21 vs frequency**  
- Find:
  - Gain value  
  - **3-dB bandwidth**

#### Reverse Isolation
- Plot **S12**

---

### 3. Noise Analysis
- Plot **Noise Figure (NF) vs frequency**  
- Evaluate LNA noise performance  

---

### 4. Linearity Analysis

#### 1-dB Compression Point
- Plot **Pout vs Pin**  
- Determine **P1dB**

#### Two-Tone Analysis
- Calculate:
  - **IIP3 (Input Third-Order Intercept Point)**  
  - Intermodulation distortion  

---

### 5. Harmonic Distortion
- For input power = **-30 dBm**:
  - Calculate:
    - **HD2 (2nd harmonic)**  
    - **HD3 (3rd harmonic)**  
  - Express in **dBc**

---

### 6. Intermodulation Analysis
- For **two-tone input (-50 dBm each)**:
  - Measure output intermodulation products  

---

##  Required Outputs

- Design calculations & approach  
- Device sizing and component values  
- DC characteristic plots:
  - Id vs Vgs  
  - Id vs Vds  
  - gm vs Vds  
- S-parameter plots:
  - S11, S21, S12  
- Noise figure plot  
- Pout vs Pin plot  
- IIP3 results  
- Harmonic distortion (HD2, HD3)  
- Intermodulation levels  

---

##  Tools Used

- Cadence Virtuoso  
- Spectre RF  
- ADE (Analog Design Environment)  

---

##  Project Structure

```bash
project/
│── schematic_lna/
│── results/
│── plots/
│── README.md
```

---

##  Learning Outcomes

- RF circuit design fundamentals  
- LNA performance metrics (gain, NF, matching)  
- S-parameter analysis  
- Linearity concepts (P1dB, IIP3)  
- Practical Cadence RF simulation flow  

---

##  Author
**Aditi Dhibar**
