In the given below circuit find the DC operating point,Gain using transient analysis and AC analysis for different values of RD and W/L ratio.

![Screenshot 2025-02-17 230832](https://github.com/user-attachments/assets/d5436a82-a51a-4b7d-b983-c42d454b6236)


DC ANALYSIS
FOR RD = 1K
The input voltage is connected to the gate terminal that is 0.9v
P = VI
ID = 55µA

W/L should match the obtained ID value, so set the aspect ratio value to obtain the 
current value.

WKT,
    Vov = VGS - VTH

    ![Screenshot 2025-02-17 203841](https://github.com/user-attachments/assets/4abec7a4-b933-47e8-b86a-501ac58f252d)



To perform DC analysis select DC operating point and run the simulation.

The obtained DC operating point is (1.74 V , 55µ A).

![image](https://github.com/user-attachments/assets/e4215347-171c-4336-bdbd-2af65b0fd501)


FOR RD = 5K

![Screenshot 2025-02-17 230931](https://github.com/user-attachments/assets/6a4bd4e1-cbaa-4f3e-ba09-7c96233ff7b5)


The Obtained DC operating value is (1.52 V , 55µ A).


![image](https://github.com/user-attachments/assets/3d8c260f-8dc3-4afb-a95c-f13d87fa34d4)

   
For W/L = 1µ/180n


![Screenshot 2025-02-17 230832](https://github.com/user-attachments/assets/fde357b3-2510-4671-9d8c-e68f501bb08d)



The opbtained DC operating point is (1.63 V,0.00016631 A).


![image](https://github.com/user-attachments/assets/e2e7afb8-7a31-40e1-89c7-17fcd8c953bb)


TRANSIENT ANALYSIS

This analysis is done to analyze the voltage change over time w.r.t input signal

select the dc sine with 
1.DC ofset voltage of 0.9v
2.Amplitude as 50 mV
3.frequency 1khz
 run the command keeping stop time to 5ms

 ![Screenshot 2025-02-17 231204](https://github.com/user-attachments/assets/97dfe95d-2723-4ede-8797-d00499907568)



 INPUT WAVEFORM:

![image](https://github.com/user-attachments/assets/9d45fa72-6732-4bec-b008-00940b9508fe)

OUTPUT WAVEFORM:

![image](https://github.com/user-attachments/assets/555f9ad6-9996-45c1-b154-f58ad2a72928)

 
GAIN:
  Vin = 1.793V
  vout = 900mv
  Av = Vout/Vin
  AV = 1.793/900*10^-3
  Av = 2

  AC ANALYSIS:

  The analysis is done based on different frequencies

select the dc sine with 
1.DC ofset voltage of 0.9v
2.Amplitude as 50 mV
3.frequency 1khz
4.select ac analysis by keeping type of sweep to decade and no. of points to 20
5. select the frequency from 0.1hz to 1Thz

![Screenshot 2025-02-17 231325](https://github.com/user-attachments/assets/45f684e0-982a-49bb-8959-c18b2d1551ce)


![image](https://github.com/user-attachments/assets/75005d14-5b08-471b-8816-854149449d68)

FREQUENCY RESPONSE:

![image](https://github.com/user-attachments/assets/59ea971e-ebe1-4596-8010-a63884fc2388)


RESULT:

1.DC OPERATING POINT
* For Rd -- 1K Ω : (1.74 V , 55µ A).
* For RD -- 5k Ω : (1.52 V , 55µ A).
* For W/L -- 1µ/180n : (1.63 V,0.00016631 A).
2.TRANSIENT ANALYSIS:
  GAIN = 2
3. AC ANALYSIS:


      INFERENCE:

  
ID = (1/2)*Kn(Vov)^2

• Increase W/L → Increases ID (for the same VGS).
• Decrease W/L → Reduces ID, requiring higher VGS to maintain the same current.




  Q2 For the given circuit below find the DC operating point, gain and AC analysis.Use P=100mW.

  ![Screenshot 2025-02-17 224214](https://github.com/user-attachments/assets/1f1ff2df-5074-4377-a7a2-f6fe62c84501)



  DC ANALYSIS

  ![Screenshot 2025-02-17 224214](https://github.com/user-attachments/assets/6aa0d2cc-a38c-46ca-9324-90ee2adf1a7b)

  
![image](https://github.com/user-attachments/assets/c1a7f948-d2d9-4d69-9708-5f963c103734)

TRANSIENT ANALYSIS:

![Screenshot 2025-02-17 224919](https://github.com/user-attachments/assets/bb5aedb1-8aa4-4a16-b5ec-d47047698562)


![image](https://github.com/user-attachments/assets/c431cc95-1d6a-416a-a1cf-b36bdeb4c75c)

AC ANALYSIS:

![Screenshot 2025-02-17 225150](https://github.com/user-attachments/assets/b07c972f-4626-4a9c-9d57-0eccaf08ad0f)

![image](https://github.com/user-attachments/assets/ab40282b-221b-417f-bad5-d733ef0ac17a)



