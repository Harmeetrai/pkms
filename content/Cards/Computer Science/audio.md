# Audio
---
[[Sound]] is a wave phenomenon, involving molecules of air being compressed and expanded under the action of some physical device.
- A speaker (or other sound generator) vibrates back and forth and produces a longitudinal pressure wave that perceived as sound. 
- Since sound is a pressure wave, it takes on continuous values, as opposed to digitized ones.
- 1-dimensional nature of sound: amplitude depend on a 1D variable, the time.
	- Input from microphone is analog signal (air movement)
	- Output is analog electric signal

## Measuring Sound
---
A bel (B) is a relative unit of measurement, i.e., ratio, and is measured using the following:
$$
log_{10} \frac{Power_A}{Power_B} \rightarrow Bel
$$
A decibel (dB) is equal to $1/10$ bel (B):
$$
10*log_{10}\frac{Power_A}{Power_B} \rightarrow decibel(dB)
$$
Two signals differ by one dB have a power ratio of $10^{1/10}$

power is proportional to the square of voltage:
$$
10*\log_{10}\frac{V^2_{\text{sound}}}{V^2_{\text{threshold of hearing}}} = 20*\log_{10}\frac{V_{\text{sound}}}{V_{\text{threshold of hearing}}}
$$

## Sampling Frequency (idk)
### Nyquist Theorem
For correct sampling we must use a sampling rate equal to at least ==twice the maximum frequency content in the signal.== This rate is called the **Nyquist rate**
## Signal to Noise Ratio (SNR)
---
Signal to Noise Ratio (SNR): the ratio of the power of the correct signal and the noise
- A common measure of the quality of the signal
- The ratio can be huge and often non-linear
So practically, SNR is also measured in logscale: decibels (dB):
$$
\text{SNR}=10*\log_{10}\frac{V^2_{signal}}{V^2_{noise}}=20*\log_{10}\frac{V_{signal}}{V_{noise}}
$$
## Quantization Noise
---
If voltages are actually in 0 to 1 but we have only 8 bits in which to store values, then effectively we force all continuous values of voltage into only 256 different values.

This introduces a roundoff error, which is often called **[[quantization noise]] (or quantization error).** The quality of the quantization is characterized by the Signal to Quantization Noise Ratio ([[SQNR]]).
$$
\text{SQNR}=20*\log_{10}\frac{V_{\text{signal}}}{V_{noise}}
$$
## Human Auditory System
---
The [[human auditory system]] has range of human’ hearing: 20Hz - 20kHz
- Hearing threshold varies dramatically at different frequencies
Masking effect:
- what we hear depends on what audio environment we are in
- One strong signal can overwhelm/ hide another
- Simultaneous masking: Two sounds occur simultaneously and one is masked by the other.
- Backward masking (Pre): A softer sound that occurs prior to a loud one will be masked by the louder sound.
- Forward masking (Post): softer sounds that occur as much as 200 milliseconds after the loud sound will also be masked.

## Example
---
**Question**: If a tuba is 20 dB louder than a singer’s voice, what is the ratio of intensities (power) of the tuba to the voice?

**Solution**: Using the decibal equation:
$$ \begin{align} 10*log_{10}\frac{Power_A}{Power_B} &= 20 \text{ dB}  \\ log_{10}\frac{Power_A}{Power_B} &= 2 \\ \\ \frac{Power_A}{Power_B} &= 10^2 = 100 \end{align} $$
Therefore, the ratio of intensities is 100 times greater than the singer's voice.

---
**Question**: Assume one violin’s sound is 65dB. (a) What is the sound level of 2 violins? (b) 5 violins? (c) 200 violins.

**Solution**: using formula $10+\log_{10}(\text{number of added sounds}) + \text{initial sound}$
1) $dB=10*\log_{10}(2)+65 =68 \text{ dB}$
2) $dB=10*\log_{10}(5)+65 =72 \text{ dB}$
3) $dB=10*\log_{10}(200)+65 =88 \text{ dB}$

---
**Question**:Assume one violin’s sound is 65dB and the corresponding mic output is 3mV. (a) What’s the mic output for a sound that is barely heard by you? (b) What is the mic output of 4 violins?
**Solution**: Part A
Let $V_{signal} = 3mV$, solving for $V_{\text{noise}}$
$$\begin{align} 20 \log_{10}V_{\frac{\text{signal}}{V_{\text{noise}}}}&=65 \text{ dB} \\ \frac{V_{\text{signal}}}{V_{\text{noise}}} &= 10^{65/20} \\ V_{\text{noise}} &= \frac{3mV}{10^{65/20}} = 0.00169 \text{ mV}\end{align}$$We need to solve for when the mic output for a sound is barely heard, which is $0 \text{dB}$$$\begin{align} 20 \log_{10}{\frac{V_\text{signal}}{V_{\text{noise}}}}&=0 \text{ dB} \\ \frac{V_\text{signal}}{V_{\text{noise}}} &=10^0 = 1 \end{align}$$Since we know $V_{\text{noise}} = 0.00169 \text{mV}$ therefore, $V_{\text{signal}} = 0.00169 \text{mV}$

**Solution**: Part B) $3*\sqrt{ 4 } = 6 \text{ mV}$

---