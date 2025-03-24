# Current mirroring circuit
Design and Analyze Current mirror circuit as active load in amplifier circuit.

Given :

Vdd=1.8 V.
P <=1 mW.
Av>-10 V/V.

circuit diagram:
![Screenshot 2025-03-24 195140](https://github.com/user-attachments/assets/21979d87-b1ef-436c-aee2-37ca1ccbb471)

#dc analysis
1:1 ratio:

The drain current with channel length modulation is expressed as:
ID = (1/2)μnCox(W/L)(VGS - Vth)^2
ITotal = P/VDD
ITotal = Iref + Ix
Since the ratio is 1:1 Iref = Ix
Iref = ITotal/2
ITotal = 1 mW/1.8 V
ITotal = 0.555 mA
Iref = 0.555 m/2
Iref = 0.2778 mA.

![Screenshot 2025-03-24 195249](https://github.com/user-attachments/assets/88c84a41-8010-4f80-a57b-6df4115a0a11)


#Transient analysis:

Change the input voltage to sine and change the amplitude to 50 mV , frequency to 1 kHz and offset voltage to 0.6275 V.

![Screenshot 2025-03-24 200257](https://github.com/user-attachments/assets/7a1df152-29e5-4515-a910-e85b15289259)


ANALYSIS
![Screenshot 2025-03-24 200056](https://github.com/user-attachments/assets/359079b4-e297-470c-80a9-4ca2c4ae3451)

![Screenshot 2025-03-24 200111](https://github.com/user-attachments/assets/0f571296-86bb-4dca-9c08-a78b1b8b110e)

The expected gain was greater than or equal to 10 V/V and the obtained gain is 13.77 V/V.


#AC ANALYSIS


![image](https://github.com/user-attachments/assets/68583fb0-4e54-4be4-b830-2a05ad27f33b)

The Expected gain in dB is 20 and the obtained gain is 26.23 dB.

#1:2 RATIO

DC ANALYSIS

Iref = 0.185 mA. In order to determine the current value based on the specified ratio, the W/L values for M2 and M3 are 6 µm/180nm and 6 µm/180nm, nd M1 is 3 µm/180nm respectively. Since Vin is chosen to be in the saturation range, the value that is provided is 0.763 V. 

![Screenshot 2025-03-24 201134](https://github.com/user-attachments/assets/938595d9-265d-4bd9-8f04-14fb500ee2c7)


TRANSIENT ANALYSIS

![Screenshot 2025-03-24 201552](https://github.com/user-attachments/assets/0379d12d-8e2b-41df-aab7-36a6edbd6bca)


![Screenshot 2025-03-24 201605](https://github.com/user-attachments/assets/da3223b7-0b3e-4abf-8c4a-611af292530d)


The expected gain was greater than or equal to 10 V/V and the obtained gain is 12.11 V/V.

AC ANALYSIS

![image](https://github.com/user-attachments/assets/40758185-52ea-4c6c-a09d-ba2b1de4786f)


Av(in dB) = 25.57dB
Av(in V/V) = 12.11


1:3 RATIO:

![Screenshot 2025-03-24 202344](https://github.com/user-attachments/assets/0dfacf5e-483e-4a1d-a360-427fcfad9553)

OUTPUT:
![Screenshot 2025-03-24 202327](https://github.com/user-attachments/assets/0a4897c4-25fd-42f9-877d-77a47bb8ec51)

TRANSIENT ANALYSIS:

![Screenshot 2025-03-24 202621](https://github.com/user-attachments/assets/41310b75-d7e4-4193-99aa-eb14f4d96235)

![Screenshot 2025-03-24 202637](https://github.com/user-attachments/assets/fe3a2080-cdc7-4b53-a577-f9c174530f2e)


The expected gain was greater than or equal to 10 V/V and the obtained gain is 13.167 V/V.

![Screenshot 2025-03-24 202827](https://github.com/user-attachments/assets/daeecdef-8ac9-441d-b0b9-7a5ebe4465c3)


![image](https://github.com/user-attachments/assets/ae8b1d77-9096-48e1-834b-8f2c0b528680)


![Screenshot 2025-03-24 203017](https://github.com/user-attachments/assets/8cc111fb-1cd6-48fc-a74b-2682144fc083)

2:1 RATIO
DC ANALYSIS

![Screenshot 2025-03-24 203418](https://github.com/user-attachments/assets/9f375b95-0c0f-44c8-9ed0-8b102d323d47)


![Screenshot 2025-03-24 203341](https://github.com/user-attachments/assets/937d1595-358a-40c8-92bc-7d124a7606f1)


TRANSIENT ANALYSIS:


![image](https://github.com/user-attachments/assets/c8d1c933-126a-4404-ae1d-4061144e79c2)


AC ANALYSIS:

![image](https://github.com/user-attachments/assets/5370c1e4-4935-4d56-877a-0e20d1bc3215)


![image](https://github.com/user-attachments/assets/7e24dcd8-9d24-42ef-9b5c-95b1c74a0294)


![image](https://github.com/user-attachments/assets/8ea374d2-e04a-4d29-8cee-dfb32803181a)


Inference :
The current mirror circuit accurately copies the reference current with very little variation, ensuring reliable current mirroring across different W/L ratios.
Even when the W/L ratio changes while keeping the same proportion, the drain current (ID) stays nearly the same, confirming the circuit's effectiveness.
The amplifier gain is slightly higher than expected due to small differences in transistor properties or minor simulation effects.
When the mirror ratio increases (from 1:1 to 1:2), the gain also increases as expected.
Overall, the results closely match theoretical predictions, proving that the simulation and circuit design are working correctly.









































