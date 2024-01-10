# MPEG Audio

MPEG Audio proceeds by first applying a filter bank to the input, to break the input into its frequency components. In parallel, it applies a [[psychoacoustic model]] to the data, and this model is used in a bit allocation block. Then the number of bits allocated is used to quantize the information from the filter bank. The overall result is that [[quantization]] provides the [[audio compression]], and bits are allocated where they are most needed to lower the quantization noise below an audible level.

MPEG audio sets out three downward-compatible layers of audio compression, each able to understand the lower layers. Each offers more complexity in the [[psychoacoustic model]] applied and correspondingly better compression for a given level of audio quality. However, an increase in complexity, and concomitantly in compression effectiveness, is accompanied by extra delay.

1. layer 1 quality can be quite good provided a comparatively high bit-rate is available
2. layer 2 has more complexity; was proposed for use in Digital Audio Broadcasting
3. layer 3 (MP3) is most complex, and was originally aimed at audio transmission over ISDN lines

## Audio Strategy

The MPEG approach to compression relies on [[quantization]], but also recognizes that the [[human auditory system]] is not accurate within the width of a [[critical band|critical band]], both in terms of perceived loudness and audibility of a test frequency. 

The encoder employs a bank of filters that act to first analyze the frequency (spectral) components of the audio signal by calculating a frequency transform of a window of signal values. Then, decompose the signal into subbands by using a bank of filters (Layer 1 & 2: “quadrature mirror”; Layer 3: adds a DCT; psychoacoustic model: Fourier transform)

[[frequency masking]] can be brought to bear by using a [[psychoacoustic model]] to estimate the just noticeable noise level. In its [[quantization]] and coding stage, the encoder balances the masking behavior and the available number of bits by discarding inaudible frequencies and scaling quantization according to the sound level left over, above masking levels.
## Algorithm

![[Pasted image 20231213212508.png]]