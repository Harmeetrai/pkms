# Distortion Measure

Distortion measure is a [[mathematics]] quantity that specifies how close an approximation is to its original, using some distortion criteria. When looking at [[compression|compressed]] data, it is natural to think of the distortion in terms of the numerical difference between the original data and the reconstructed data. However, when the data to be compressed is an image, such a measure may not yield the intended result.

Distortion is measured using the **Mean Squared Error (MSE)**:\delta
$$
σ_{d}^2 = \frac{1}{N}\sum_{n=1}^{N}(x_{n}-y_{n})^2
$$
If we are interested in the size of the error relative to the signal, we can measure the signal-to-noise ratio ([[SNR]]) by taking the ratio of the average square of the original data sequence and the Mean Squared Error (MSE):
$$
\text{SNR} = 10\log_{10}\frac{σ_{x}^2}{σ_{d}^2}
$$

## Rate-Distortion Theory
Lossy compression always involves a trade-off between rate and distortion. Rate is the average number of bits required to represent each source symbol. Within this framework, the trade-off between rate and distortion is represented in the form of a rate-distortion function $R(D)$.

![[Pasted image 20231212154838.png]]