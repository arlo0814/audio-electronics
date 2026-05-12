# Filter Analysis
## Input Filter
$$f_c = \frac{1}{2\pi \cdot R_{31} \cdot C_{21}} = \frac{1}{2\pi(1000)(470 \cdot 10^{-12})} = 338.6 \text{ kHz (low-pass)}$$
$$f_c = \frac{1}{2\pi \cdot R_{32} \cdot C_{23}} = \frac{1}{2\pi(47000)(2.2 \cdot 10^{-6})} = 1.539 \text{ Hz (high-pass)}$$

## Active Filter Stage
$$L_{eq} = R_{series} \cdot R_{bias} \cdot C_{gyr} = (560)(47000)(470 \cdot 10^{-12})$$
$$L_{eq} = 12.37 \text{ mH}$$$$f_o = \frac{1}{2\pi\sqrt{L_{eq} \cdot C_{res}}} = \frac{1}{2\pi\sqrt{(12.37 \cdot 10^{-3})(4.7 \cdot 10^{-9})}}$$
$$f_o = 20.87 \text{ kHz}$$$$Q = \frac{1}{R_{series}}\sqrt{\frac{L_{eq}}{C_{res}}} = \frac{1}{560}\sqrt{\frac{12.37 \cdot 10^{-3}}{4.7 \cdot 10^{-9}}}$$
$$Q = 2.897$$$$BW = \frac{f_o}{Q} = \frac{20.87 \cdot 10^3}{2.897}$$
$$BW = 7204 \text{ Hz}$$$$f_L = f_o - \frac{BW}{2} = 20.87 \cdot 10^3 - \frac{7204}{2} = 17.27 \text{ kHz}$$
$$f_H = f_o + \frac{BW}{2} = 20.87 \cdot 10^3 + \frac{7204}{2} = 24.47 \text{ kHz}$$
