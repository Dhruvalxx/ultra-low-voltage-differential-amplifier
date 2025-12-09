# Ultra-Low-Voltage (450mV) Differential Amplifier Design

[![Technology](https://img.shields.io/badge/Technology-180nm_CMOS-blue)](https://github.com/Dhruvalxx/ultra-low-voltage-differential-amplifier)
[![Power](https://img.shields.io/badge/Power-432nW-green)](https://github.com/Dhruvalxx/ultra-low-voltage-differential-amplifier)
[![Gain](https://img.shields.io/badge/Gain-25.2dB-orange)](https://github.com/Dhruvalxx/ultra-low-voltage-differential-amplifier)

## 📋 Project Overview

This project presents the design and simulation of an **ultra-low-voltage differential amplifier** operating at **450mV supply** using subthreshold-biased MOSFETs in **180nm CMOS technology**. The design achieves exceptional power efficiency (432nW) while maintaining MHz-range bandwidth, making it suitable for biomedical sensors, IoT devices, and energy harvesting applications.

---

## ⚡ Key Performance Results

| Parameter | Value | Unit |
|-----------|-------|------|
| **Supply Voltage** | 450 | mV |
| **Power Consumption** | 432 | nW |
| **Voltage Gain** | 25.2 | dB |
| **Unity Gain Frequency** | 10.1 | MHz |
| **3dB Bandwidth** | 1.47 | MHz |
| **CMRR** | 24.06 | dB |
| **Input-Referred Noise** | 2.2×10⁻⁹ | V²/Hz |
| **Technology** | GPDK 180nm | CMOS |

---

## 🎯 Design Highlights

### **Circuit Architecture**
- **Topology:** Fully differential input stage with current mirror active load
- **Biasing:** All transistors operated in subthreshold region (weak inversion)
- **Configuration:** Single-stage design with PMOS current mirror load

### **Key Design Features**
✅ **Subthreshold Operation:** Exploits exponential I-V relationship for maximum power efficiency  
✅ **Current Mirror Load:** PMOS active load maximizes output impedance and voltage gain  
✅ **Ultra-Low Power:** Achieves 1000× power reduction compared to strong inversion designs  
✅ **Systematic Optimization:** DC, AC, and transient analysis for complete characterization  

### **Transistor Dimensions**
- **PMOS Load (Q3, Q4):** W = 80µm, L = 180nm
- **NMOS Input Pair (Q1, Q2):** W = 40µm, L = 180nm  
- **Tail Current Source (Q5):** W = 40µm, L = 180nm

### **Bias Conditions**
- **Tail Bias Voltage:** 350mV (ensures subthreshold operation)
- **Input DC Level:** 270mV
- **Differential Input:** 10mV amplitude @ 10kHz

---

## 🛠️ Design Tools & Methodology

### **EDA Tools**
- **Design Entry:** Cadence Virtuoso Schematic Editor
- **Simulation:** Cadence Spectre Circuit Simulator
- **Technology:** GPDK 180nm CMOS Process Design Kit
- **Analysis:** DC Operating Point, AC Frequency Response, Transient, Noise

### **Design Methodology**
1. **Technology Selection:** 180nm CMOS for balance between performance and manufacturability
2. **Operating Point:** Systematic selection of VGS < VTH for all transistors
3. **Transistor Sizing:** Optimized W/L ratios for transconductance vs. power trade-off
4. **Load Design:** Current mirror topology for enhanced output impedance
5. **Verification:** Comprehensive simulation across DC, AC, transient, and noise domains

---

## 📊 Performance Analysis

### **DC Analysis**
- All transistors confirmed in subthreshold region (VGS < VTH)
- Stable bias point with adequate voltage headroom
- Differential pair properly balanced

### **AC Analysis**
- **Voltage Gain:** 18.26 V/V (25.2 dB)
- **Unity Gain Frequency:** 10.1 MHz
- **3dB Bandwidth:** 1.47 MHz
- **Phase Margin:** Adequate for stability

### **Transient Analysis**
- Low distortion with 10mV differential input
- Fast settling time
- Linear amplification within operating range

### **Noise Analysis**
- **Dominant Contributors:** NMOS differential pair (72%)
- **Output Noise:** 4.27×10⁻⁷ V²/Hz @ 1kHz
- **Input-Referred Noise:** 2.2×10⁻⁹ V²/Hz

### **Comparison with Literature**

| Reference | Tech | VDD | Gain | Power | UGF |
|-----------|------|-----|------|-------|-----|
| **This Work** | 180nm | 0.45V | 25.2dB | **432nW** | 10.1MHz |
| He et al. 2009 | 130nm | 0.5V | 51dB | 600µW | 112MHz |
| Majumder 2015 | 45nm | ±0.4V | 74.6dB | 390µW | 1MHz |
| Magnelli 2013 | 180nm | 0.5V | 70dB | 75nW | 18kHz |

**Key Achievement:** Best power-bandwidth trade-off (10.1MHz @ 432nW)

---

## 📈 Target Applications

This ultra-low-power amplifier is ideal for:

- 🏥 **Biomedical Sensors:** ECG, EEG signal conditioning
- 📡 **Wireless Sensor Networks:** Battery-powered IoT nodes
- 🔋 **Energy Harvesting Systems:** Ultra-low threshold startup circuits
- 📱 **Portable Medical Devices:** Continuous health monitoring
- 🎧 **Hearing Aids:** Low-power audio preamplifiers
- 🌡️ **Environmental Monitoring:** Temperature/humidity sensors

---

## 📄 Complete Documentation

**Full design report including circuit schematics, simulation results, and analysis:**  
📘 **[View Design Report (PDF)](Design_Report.pdf)**

**Report Contents:**
- Introduction & Background
- Design Specifications & Methodology
- Circuit Architecture & Transistor Sizing
- Simulation Results (DC/AC/Transient/Noise)
- Performance Comparison with State-of-the-Art
- Conclusions & Future Work

---

## 🔬 Technical Insights

### **Why Subthreshold Operation?**
Operating transistors in weak inversion (VGS < VTH) provides:
- **Exponential gm/ID:** Higher transconductance per unit current
- **Low Voltage Headroom:** ~100mV saturation voltage vs. 200mV+ in strong inversion
- **Superior Power Efficiency:** 1000× improvement for same performance
- **Energy Harvesting Compatibility:** Operates from solar cells, thermoelectric generators

### **Design Challenges & Solutions**

| Challenge | Solution |
|-----------|----------|
| Limited voltage headroom @ 450mV | Subthreshold operation reduces VDS,sat |
| Low gain from single stage | Current mirror load boosts output impedance |
| Temperature sensitivity | Systematic corner analysis across PVT |
| Noise in subthreshold | Careful transistor sizing and bias current selection |

---

## 🚀 Future Enhancements

Potential improvements for next iteration:

- [ ] **Cascode Configuration:** Boost gain by 20-30dB using cascoded loads
- [ ] **Adaptive Biasing:** Temperature compensation circuitry
- [ ] **Two-Stage Design:** Miller compensation for 60-80dB gain
- [ ] **Multi-VTH Devices:** Mixed VTH design for better performance
- [ ] **Layout Implementation:** Physical design and post-layout simulation
- [ ] **Fabrication:** Tapeout and silicon validation

---

## 🎓 Academic Information

**Course:** Analog and Custom IC Design (ACIC)  
**Institution:** Institute of Technology, Nirma University  
**Semester:** VII (Fall 2024)  
**Date:** December 2024  

**Team Members:**
- Devanshu Parikh (22BEC029)
- Dhruval Vachhani (22BEC034)

---

## 📧 Contact

**Dhruval Vachhani**  
📧 Email: dhruvalvachhani@gmail.com  
🔗 LinkedIn: [linkedin.com/in/dhruvalvachhani](https://linkedin.com/in/dhruvalvachhani)  
💼 GitHub: [github.com/Dhruvalxx](https://github.com/Dhruvalxx)  
📱 Phone: +91 8160519378

---

## 📚 References

[1] L. Magnelli et al., "Design of a 75-nW, 0.5-V subthreshold CMOS operational amplifier," *Int. J. Circuit Theory Appl.*, vol. 42, no. 9, pp. 967–977, 2014.

[2] X.-Y. He et al., "A 0.5-V wideband amplifier for a 1-MHz CT complex ΔΣ modulator," *IEEE Trans. Circuits Syst. II*, vol. 56, no. 11, pp. 805–809, 2009.

[3] D. Majumder et al., "An ultralow-power low-voltage class-AB fully differential op amp," *Proc. Int. Conf. Ind. Instrum. Control*, pp. 1089–1093, 2015.

[4] B. Razavi, *Design of Analog CMOS Integrated Circuits*, 2nd ed. McGraw-Hill Education, 2017.

---

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## ⭐ Acknowledgments

Special thanks to Prof. Hardik Joshi for guidance and the Institute of Technology, Nirma University for providing access to Cadence design tools and GPDK 180nm PDK.

---

<div align="center">

**If you find this project useful, please consider giving it a ⭐!**

*Designed with ❤️ for ultra-low-power analog IC design*

</div>
```

5. Scroll down and click **"Commit changes"**
6. Commit message: `Update README with complete project documentation`
7. Click **"Commit changes"**

---

## **STEP 4: ADD TOPICS/TAGS**

1. Go back to your repository main page
2. Click the ⚙️ **gear icon** next to "About" (top right)
3. Add these topics (press Enter after each):
   - `analog-ic-design`
   - `differential-amplifier`
   - `cadence-virtuoso`
   - `ultra-low-power`
   - `subthreshold-operation`
   - `180nm-cmos`
   - `vlsi-design`
   - `biomedical-sensors`

4. Click **"Save changes"**

---

## **DONE! ✅**

Your repository now has:
1. ✅ Professional README with all key information
2. ✅ Complete PDF report
3. ✅ MIT License
4. ✅ Relevant topics for discoverability

**Repository structure:**
```
ultra-low-voltage-differential-amplifier/
├── README.md ✓
├── Design_Report.pdf ✓
└── LICENSE ✓
```

---

## **FINAL STEP: UPDATE YOUR RESUME**

Add this line to your resume project entry:
```
ULTRA-LOW-VOLTAGE DIFFERENTIAL AMPLIFIER DESIGN          Dec 2024
Cadence Virtuoso | GPDK 180nm | Spectre | DC/AC/Transient Analysis
Repository: github.com/Dhruvalxx/ultra-low-voltage-differential-amplifier

- Designed ultra-low-power differential amplifier in 180nm CMOS operating at 450mV 
  achieving 25.2dB gain, 10.1MHz unity gain frequency, and 432nW power consumption 
  through systematic subthreshold biasing optimization
- Implemented current mirror active load topology maximizing output impedance while 
  achieving clean DC, AC, and transient response with CMRR of 24.06dB and 
  input-referred noise of 2.2×10⁻⁹ V²/Hz
- Achieved 1000× power reduction compared to strong-inversion designs through 
  subthreshold operation while maintaining MHz-range bandwidth suitable for 
  biomedical sensor applications
- Conducted comprehensive DC operating point analysis, AC frequency response 
  characterization, and transient settling behavior verification using Cadence 
  Spectre simulator
