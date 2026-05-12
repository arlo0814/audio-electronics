# Filter Analysis
## Input Filter
$$f_c = \frac{1}{2\pi \cdot R_{31} \cdot C_{21}} = \frac{1}{2\pi(1000)(470 \cdot 10^{-12})} = 338.6 \text{ kHz (low-pass)}$$
$$f_c = \frac{1}{2\pi \cdot R_{32} \cdot C_{23}} = \frac{1}{2\pi(47000)(2.2 \cdot 10^{-6})} = 1.539 \text{ Hz (high-pass)}$$

## Active Filter 
### Calculations for one band
$$L_{eq} = R_{series} \cdot R_{bias} \cdot C_{gyr} = (560)(47000)(470 \cdot 10^{-12})$$
$$L_{eq} = 12.37 \text{ mH}$$$$f_o = \frac{1}{2\pi\sqrt{L_{eq} \cdot C_{res}}} = \frac{1}{2\pi\sqrt{(12.37 \cdot 10^{-3})(4.7 \cdot 10^{-9})}}$$
$$f_o = 20.87 \text{ kHz}$$$$Q = \frac{1}{R_{series}}\sqrt{\frac{L_{eq}}{C_{res}}} = \frac{1}{560}\sqrt{\frac{12.37 \cdot 10^{-3}}{4.7 \cdot 10^{-9}}}$$
$$Q = 2.897$$$$BW = \frac{f_o}{Q} = \frac{20.87 \cdot 10^3}{2.897}$$
$$BW = 7204 \text{ Hz}$$$$f_L = f_o - \frac{BW}{2} = 20.87 \cdot 10^3 - \frac{7204}{2} = 17.27 \text{ kHz}$$
$$f_H = f_o + \frac{BW}{2} = 20.87 \cdot 10^3 + \frac{7204}{2} = 24.47 \text{ kHz}$$

### Tabulated values for each band
| Band | $C_{gyr}$ | $C_{res}$ | $L_{eq}$ | $f_0$ | $Q$ | $BW$ | $f_L$ | $f_H$ |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 220 nF | 2.2 uF | 5.790 H | 44.59 Hz | 2.897 | 15.39 Hz | 36.90 Hz | 52.29 Hz |
| 2 | 100 nF | 1 uF | 2.632 H | 98.10 Hz | 2.897 | 33.86 Hz | 81.17 Hz | 115 Hz |
| 3 | 47 nF | 470 nF | 1.237 H | 208.7 Hz | 2.897 | 72.04 Hz | 172.7 Hz | 244.7 Hz |
| 4 | 22 nF | 220 nF | 579.0 mH | 305.1 Hz | 2.897 | 105.3 Hz | 252.5 Hz | 357.8 Hz |
| 5 | 10 nF | 100 nF | 263.3 mH | 980.8 Hz | 2.898 | 338.4 Hz | 811.6 Hz | 1.15 kHz |
| 6 | 4.7 nF | 47 nF | 123.7 mH | 2.087 kHz | 2.897 | 720.4 Hz | 1.727 kHz | 2.447 kHz |
| 7 | 3.3 nF | 33 nF | 88.86 mH | 2.939 kHz | 2.930 | 1.003 kHz | 2.438 kHz | 3.441 kHz |
| 8 | 2.2 nF | 22 nF | 57.90 mH | 4.459 kHz | 2.897 | 1.539 kHz | 3.690 kHz | 5.229 kHz |
| 9 | 1 nF | 10 nF | 26.32 mH | 9.810 kHz | 2.897 | 3.386 kHz | 8.117 kHz | 11.5 kHz |
| 10 | 470 pF | 4.7 nF | 12.37 mH | 20.87 kHz | 2.897 | 7.204 kHz | 17.27 kHz | 24.47 kHz |

## Output Filter Stage
$$A_v = 1 + \frac{R_f}{R_{gyr}} = 1 + \frac{3300}{560} = 6.893$$
$$A_{v-dB} = 20 \log(6.893) = 16.77 \text{ dB}$$
$$f_{c-H} = \frac{1}{2\pi \cdot R_f \cdot C_{22}} = \frac{1}{2\pi(3300)(470 \cdot 10^{-12})} = 102.6 \text{ kHz}$$
$$f_{c-L} = \frac{1}{2\pi \cdot R_{Load} \cdot C_{24}} = \frac{1}{2\pi(10000)(1 \cdot 10^{-6})} = 15.92 \text{ Hz}$$
