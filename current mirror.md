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































