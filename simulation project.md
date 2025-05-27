Cascode Telescopic Differential Amplifier and Folded Cascode OTA


 
Keerthana KN Electronics and Communication
Engineering Mysuru
2023ec keerthanakn_a@nie.ac.in
 
Mahadev Yankanna Malali Electronics and Communication
Engineering Mysuru
2023ec_mahadevyankannamalali_a@nie.ac.in 


MP Hemanth Kumar Electronics and Communication
Engineering Mysuru
2023ec_mphemanthkumar_a@nie.ac.in
 
Nandan B Electronics and Communication
Engineering Mysuru
2023ec_nandanb_a@nie.ac.in  

 
Abstract— This work presents the design and analysis of two high-performance analog amplifier topologies: the Cascode Telescopic Differential Amplifier and the Folded Cascode Operational Transconductance Amplifier (OTA). The Telescopic Cascode Amplifier offers superior gain and bandwidth due to its stacked transistor architecture, making it well-suited for high-speed and low-noise applications. However, its limited output swing constrains its use in low-voltage environments. To address this, the Folded Cascode OTA is explored as an alternative, leveraging a current folding technique that enhances output swing and common-mode input range while maintaining high gain. Comparative performance metrics including gain, bandwidth, power consumption, and input/output voltage range are evaluated through simulation in a standard CMOS process. The results highlight the trade-offs between the two architectures, providing insights into optimal topology selection based on application requirements.

I.	INTRODUCTION
Operational amplifiers (op-amps) are fundamental building blocks in analog and mixed-signal integrated circuits, widely used in signal processing, data conversion, and communication systems. Among the various op-amp topologies, the Cascode Telescopic Differential Amplifier and the Folded Cascode Operational Transconductance Amplifier (OTA) are popular choices for applications requiring high gain, wide bandwidth, and low power consumption.
The Telescopic Cascode Amplifier is known for its excellent high-frequency performance, attributed to the reduced Miller effect and high output impedance achieved through cascode stacking. This topology is often preferred in high-speed and low-noise applications, such as high-resolution analog-to-digital converters and data acquisition systems. However, one major limitation of the telescopic architecture is its restricted output voltage swing, which becomes more pronounced in modern low-voltage CMOS processes.To overcome this constraint, the Folded Cascode OTA introduces a current folding mechanism, allowing for greater voltage headroom and improved input/output swing without sacrificing gain significantly. This makes it more suitable for low-voltage and low-power applications, such as portable electronics and biomedical devices.
This study investigates and compares both amplifier topologies in terms of their design principles, advantages, limitations, and performance metrics. By understanding the trade-offs between these architectures, designers can make informed decisions when selecting the optimal configuration for specific application requirements.


II.	DESIGN OVERVIEW

1.	Cascode Telescopic Differential Amplifier

The Cascode Telescopic Differential Amplifier is a high-gain, low-noise amplifier structure composed of a differential input pair with cascode transistors stacked above each branch. The core design consists of:
Differential input stage: Typically uses NMOS or PMOS transistors for better transconductance.
Cascode transistors: Connected above the input pair to increase output resistance and reduce the Miller effect.
Current sources: Provide biasing for both the input differential pair and cascode stages.
Load: Usually implemented as active current mirrors for high output impedance.
This topology offers high gain and excellent bandwidth due to its reduced parasitic capacitance and enhanced output resistance. However, the stacking of multiple transistors limits the output swing, making it less suitable for low-voltage designs.

2.	Folded Cascode Operational Transconductance Amplifier (OTA)

The Folded Cascode OTA modifies the telescopic structure by "folding" the current from the input pair into a different branch, improving voltage headroom. The design includes:
Differential input pair: Usually NMOS (for higher transconductance) that drives PMOS cascode devices.
Folding mechanism: The current from the input NMOS devices is folded into PMOS devices, which allows the circuit to avoid stacking all transistors vertically.
Cascode transistors: Maintain high output impedance and gain.
Output stage: Typically a current mirror or load that provides a single-ended output.
This design enhances output swing, common-mode input range, and power efficiency, making it ideal for low-voltage, low-power applications, while still offering moderate to high gain and bandwidth.
 



XXX-X-XXXX-XXXX-X/XX/$XX.00 ©20XX IEEE






I.	Fig 1. Cascode Telescopic Differential Amplifier
Technology and Supply Parameters
•	CMOS Technology: 180 nm
•	V<sub>DD</sub>: 1.8 V
•	Target Gain: > 60 dB
•	Bias Current (I<sub>bias</sub>): 100 µA
•	Load Capacitance (C<sub>L</sub>): 1 pF
•	Overdrive Voltage (V<sub>ov</sub>): 200 mV
Design Description
Telescopic Cascode Differential Amplifier
The Telescopic Cascode Amplifier is designed for high gain and low noise in high-speed analog applications. The name "telescopic" refers to the vertical stacking of transistors, which gives it a compact structure but limits voltage headroom.
Circuit Components and Function:
•	M1 and M2 (Differential Pair):
o	NMOS transistors that form the input stage.
o	Convert differential input voltage into differential current.
o	Biased by a constant current source (tail current).
•	M3 and M4 (NMOS Cascode Devices):
o	Cascode transistors placed above M1 and M2.
o	Improve output impedance and isolate Miller capacitance.
o	Boost gain by increasing effective output resistance.
•	M5 and M6 (PMOS Cascode Current Mirrors):
o	Act as active loads.
o	Mirror and combine the currents from each branch.
o	Ensure symmetrical operation and help drive a single-ended output.
•	M7 (Tail Current Source):
o	Provides a stable bias current for the differential pair.
o	Typically implemented using a wide-channel NMOS transistor or current mirror.
Key Characteristics:
•  High gain due to the cascode stacking.
•  Limited output swing, since each transistor stage consumes voltage headroom.
•  High-speed operation due to low parasitic capacitance.



                        2.  Fig 2. Folded Cascode (OTA)


•	Architecture: CMOS Folded Cascode Op-Amp
•	Technology: 180 nm CMOS
•	Supply Voltage (VDD): 1.8 V
•	Input Signal: 1mV (sine wave)
•	DC Gain: ≥ 60 dB
•	Unity Gain Bandwidth (UGBW): ~10 MHz
•	Phase Margin: ~60°

Design Description
The proposed design is a two-stage CMOS operational amplifier based on a folded cascode architecture. The first stage consists of a differential input pair with active current mirrors to achieve high gain and common-mode rejection, while the second stage is a common-source amplifier that boosts output swing and drives the load. Frequency compensation is applied using a Miller capacitor to ensure stability and achieve the desired phase margin. Transistor dimensions (W/L ratios) and bias currents are carefully optimized to meet the specifications of 120 dB gain, 50 MHz bandwidth, 0.825 V output swing, and 8 mW power consumption under a 3.3 V supply. The entire design is implemented and analyzed using LTspice
 
 Open-Loop Gain (Aₒ):
Target = 120 dB → Aₒ = 10⁶ = gm × ro (stage 1) × gain (stage 2)
- Unity Gain Bandwidth (UGBW):
UGBW = gm / Cc → For gm = 1 mS, Cc = 20 pF → UGBW = 50 MHz
- Slew Rate (SR):
SR = I / Cc → For Cc = 20 pF, SR = 1 V/µs → I = 20 µA
- Power Consumption:
P = VDD × I = 3.3 V × 2.4 mA = 7.92 mW ≈ 8 mW
- Output Swing:
Max swing = VDD / 4 = 0.825 V

III.	RESULT

INPUT:
  
          OUTPUT:
 
                   Fig .3 Folded Cascode (OTA)


OPERATING POINTS
Headings, or heads, are organizational devices that guide the reader through your paper. There are two types: component heads and text heads.
Component heads identify the different components of your paper and are not topically subordinate to each other. Examples include Acknowledgments and References and, for these, the correct style to use is “Heading 5”. Use “figure caption” for your Figure captions, and “table head” for your table title. Run-in heads, such as “Abstract”, will require you to apply a style (in this case, italic) in addition to the style provided by the drop down menu to differentiate the head from the text.






     

            


            TRANSIENT ANALYSIS
            AC ANALYSIS
             Fig 4. Cascode Telescopic Differential Amplifier


OPERATING POINTS 









IV.	CONCLUSION

In this work, the design, analysis, and comparison of two widely used analog amplifier topologies—the Telescopic Cascode Differential Amplifier and the Folded Cascode Operational Transconductance Amplifier (OTA)—were presented. Both architectures demonstrate distinct advantages and are chosen based on specific application requirements.
The Telescopic Cascode Amplifier offers superior gain and low power consumption due to its simple, vertically stacked structure. However, its performance is constrained by limited output voltage swing and reduced input common-mode range, making it less ideal for low-voltage applications.
In contrast, the Folded Cascode OTA overcomes these limitations by “folding” the current path, allowing for greater headroom, better output swing, and wider common-mode input range. Although it introduces slightly more complexity and consumes more power, it is better suited for low-voltage and portable analog systems.
Ultimately, the choice between the two topologies depends on the design priorities—gain and simplicity favor the telescopic approach, while output swing and flexibility make the folded cascode a more versatile solution in modern CMOS design.
Specification	Telescopic Cascode Amplifier	Folded Cascode OTA
		
Technology Node	180 nm CMOS	180 nm CMOS
Supply Voltage (VDD)	1.8 V	1.8 V
DC Gain	60–80 dB	50–70 dB
Unity Gain Bandwidth (UGB)	10–50 MHz	5–30 MHz
Input Common-Mode Range	Narrow (~0.6–1.2 V)	Wide (~0.3–1.5 V)
Output Swing (Peak-to-Peak)	~0.8–1.0 V	~1.2–1.4 V
Slew Rate	Moderate (5–10 V/µs)	Higher (10–20 V/µs)
Power Consumption	Lower (≤ 1 mW)	Moderate (1–2 mW)
Noise Performance	Lower (better for low-noise design)	Slightly higher
CMRR (Common-Mode Rejection)	> 60 dB	> 60 dB
		
Design Complexity	Moderate	Higher (more biasing branches)
Best Use Case	High-speed, low-noise applications	Low-voltage, high swing designs
 




COMPARISION TABLE :




V.	REFERENCE

1. Behzad Razavi, “ Design of Analog CMOS Integrated Circuit”, Tata McGraw Hill 2001.
2. Sudhir.M.Mallya, Joseph.H.Nevin, “Design Procedures for a fully differential Folded Cascode CMOS operational Amplifier”, IEEE Journal of Solid-State Circuits, Vol.24, No.6, December 1989,pp 1737-1740. I. S. Jacobs and C. P. Bean, “Fine particles, thin films and exchange anisotropy,” in Magnetism, vol. III, G. T. Rado and H. Suhl, Eds. New York: Academic, 1963, pp. 271–350.
3. Katsufumi Nakamura and L. Richard Carley, “A Current – based positive-feedback technique for efficient cascode bootstrapping”, in 1991 Symposium on VLSI Circuits Digest Technical Papers, May 1991, pp 107-108.
4. K.Nakamura and L.R. Carley, “An enhanced fully differential folded cascode op-amp”, IEEE Journal of Solid-State Circuits, Vol.27,No.4 APR.1992.
4. Vimala, P., Rao, R. D., Gokhale, C. G., & Aneesh, V. S. (2024). Design of Two Stage Miller Compensated CMOS Opamp with Nulling Resistor in 90nm Technology.
5.  Sedra, A. S., & Smith, K. C. (2014). Microelectronic Circuits (7th ed.). Oxford University Press.
6. Razavi, B. (2001). Design of Analog CMOS Integrated Circuits. McGraw-Hill Education.

