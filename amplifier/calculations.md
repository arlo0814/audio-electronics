# Overview
The following calculations are from the analysis of the stages of the amplifier
<img width="829" height="449" alt="image" src="https://github.com/user-attachments/assets/ed9faf74-6491-4ddd-976d-00036ab4a68f" />

<img width="793" height="446" alt="image" src="https://github.com/user-attachments/assets/1f9a7aca-9358-43da-bb84-c09d549d61a2" />

## Input Differential Stage

$$I_{tail} \approx \frac{V_{CC} - V_{D1}}{R_4} = \frac{24.06 - 0.7}{8.2 \times 10^3}$$$$I_{tail} \approx 2.85\text{ mA}$$$$I_C \approx I_E = \frac{2.85}{2} = 1.43\text{ mA}$$$$r_e = \frac{26\text{ mV}}{I_C} = \frac{26\text{ mV}}{1.43\text{ mA}} = 18.18\text{ }\Omega$$$$A_v = \frac{R_3}{2 \cdot r_e} = \frac{470\text{ }\Omega}{2 \cdot 18.18\text{ }\Omega} = 12.93$$$$A_i = h_{FE} \approx 200$$

## Voltage Amplification Stage

$$V_{B3} = I_{C1} R_3 = (1.43\text{ mA})(470\text{ }\Omega) = 0.6721\text{ V}$$$$V_{E3} = V_{B3} - 0.7 = 0.6721 - 0.7 = -0.0279\text{ V}$$$$I_{C3} = \frac{V_{CC} - V_{D2} - V_{D4}}{R_7 + R_9} = \frac{24.06 - 0.7 - 0.7}{3.9 \times 10^3 + 5.6 \times 10^3} = 2.385\text{ mA}$$$$r_e = \frac{26\text{ mV}}{I_{C3}} = \frac{26\text{ mV}}{2.385\text{ mA}} = 10.90\text{ }\Omega$$$$g_m = \frac{1}{r_e} = \frac{1}{10.90\text{ }\Omega} = 91.74\text{ mS}$$$$A_v = g_m \cdot R_L = (91.74 \times 10^{-3})(100 \times 10^3) = 9174$$$$A_i = h_{FE} \approx 100$$

## Driver Stage

$$V_{bias} = V_{D2} + V_{D4} + (I_{C3} \cdot R_{10}) = 0.7 + 0.7 + (2.385 \times 10^{-3} \cdot 150)$$$$V_{bias} = 1.758\text{ V}$$$$I_{q\text{-driver}} = \frac{V_{bias} - (V_{BE5} + V_{BE4})}{R_{12} + R_{11}} = \frac{1.758 - (0.7 + 0.7)}{100 + 10}$$$$I_{q\text{-driver}} = 3.255\text{ mA}$$$$r_e = \frac{26\text{ mV}}{I_{q\text{-driver}}} = \frac{26\text{ mV}}{3.255\text{ mA}} = 7.988\text{ }\Omega$$$$A_v = \frac{R_L}{R_L + r_e} \approx 1$$$$A_i = h_{FE} \approx 50$$

## Power Output Stage

$$I_{q\text{-out}} = \frac{V_{bias} - (V_{BE\text{-power}} + V_{BE\text{-driver}})}{R_{11} + R_{12} + R_{16} + R_{17}} = \frac{1.785 - (0.7 + 0.7)}{10 + 100 + 0.47 + 0.47}$$$$I_{q\text{-out}} = 3.470\text{ mA}$$$$A_v = \frac{R_L}{R_L + r_e + R_E} \approx 1$$$$A_i = h_{FE} \approx 60$$

## Total Gain

$$A_{v\text{-total}} = A_{v\text{-input}} \cdot A_{v\text{-VAS}} \cdot A_{v\text{-driver}} \cdot A_{v\text{-pout}}$$$$A_{v\text{-total}} = 12.93 \cdot 9174 \cdot 1 \cdot 1$$$$A_{v\text{-total}} = 118619.82$$$$A_{v\text{-dB}} = 20 \log(118619.82)$$$$A_{v\text{-dB}} = 101.48\text{ dB}$$$$A_{i\text{-total}} = A_{i\text{-input}} \cdot A_{i\text{-VAS}} \cdot A_{i\text{-driver}} \cdot A_{i\text{-pout}}$$$$A_{i\text{-total}} = 200 \cdot 100 \cdot 50 \cdot 60$$$$A_{i\text{-total}} = 60,000,000$$$$A_{i\text{-dB}} = 20 \log(60,000,000)$$$$A_{i\text{-dB}} = 155.56\text{ dB}$$$$A_{p\text{-total}} = A_{v\text{-total}} \cdot A_{i\text{-total}}$$$$A_{p\text{-total}} = 118619.82 \cdot 60,000,000$$$$A_{p\text{-total}} = 7.117 \times 10^{12}$$$$A_{p\text{-dB}} = 10 \log(7.117 \times 10^{12})$$$$A_{p\text{-dB}} = 128.52\text{ dB}$$



