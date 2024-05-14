


Established in 1947, the International Standards Organization (ISO) is a multinational body dedicated to worldwide agreement on international standards. An ISO standard that covers all aspects of network communications is the Open Systems Interconnection (OSI) model. It was first introduced in the late 1970s.


| OSI Layers  | Function Provided                                               |
| ----------- | --------------------------------------------------------------- |
| Application | Network application such as file transfer and terminal emulator |
| Presentaion | Data formatting and encryption                                  |
| Session     | Establishment and maintenance of session                        |
| Transport   | Provision for end-to-end reliable and unreliable delivery       |
| Network     | Delivery of packets of information, which includes routing      |
| Data Link   | Transfer of units of information, framing and error checking    |
| Physical    | Transmission of binary data of a medium                         |







[Static vs Dynamic Routing Explained | CompTIA Network+ (youtube.com)](https://www.youtube.com/watch?v=Gxdzj52hfi0&ab_channel=ByteBite)

[ByteByteGo - YouTube](https://www.youtube.com/@ByteByteGo/search?query=network)

[What Is a Computer Network? Definition, Objectives, Components, Types, and Best Practices - Spiceworks](https://www.spiceworks.com/tech/networking/articles/what-is-a-computer-network/)










# Physical Layer


## Analog and Digital

To be transmitted, data must be transformed to electromagnetic signals.

Data can be analog or digital. The term analog data refers to information that is continuous; digital data refers to information that has discrete states. Analog data take on continuous values. Digital data take on discrete values.


Data can be analog or digital. Analog data are continuous and take continuous values. Digital data have discrete states and take discrete values.


Signals can be analog or digital. Analog signals can have an infinite
number of values in a range; digital signals can have only a limited
number of values. 

In data communications, we commonly use periodic analog signals and nonperiodic digital signals.



#### Periodic Analog Signals

Periodic analog signals can be classified as simple or composite. A simple periodic analog signal, a sine wave, cannot be decomposed into simpler signals. A composite periodic analog signal is composed of multiple sine
waves.


- Frequency and period are the inverse of each other.
- Frequency is the rate of change with respect to time.
- Change in a short span of time means high frequency.
- Change over a long span of time means low frequency.
- If a signal does not change at all, its frequency is zero.
- If a signal changes instantaneously, its frequency is infinite.
- Phase describes the position of the waveform relative to time 0.
- A complete sine wave in the time domain can be represented by one single spike in the frequency domain.
- A single-frequency sine wave is not useful in data communications; we need to send a composite signal, a signal made of many simple sine waves.
- According to Fourier analysis, any composite signal is a combination of simple sine waves with different frequencies, amplitudes, and phases.
- If the composite signal is periodic, the decomposition gives a series of signals with discrete frequencies; if the composite signal is  nonperiodic, the decomposition gives a combination of sine waves with continuous frequencies.
- The bandwidth of a composite signal is the difference between the highest and the lowest frequencies contained in that signal.


#### Digital Signal


- A digital signal is a composite analog signal with an infinite bandwidth.
- Baseband transmission of a digital signal that preserves the shape of the digital signal is possible only if we have a low-pass channel with an infinite or very wide bandwidth.
- In baseband transmission, the required bandwidth is proportional to the bit rate; if we need to send bits faster, we need more bandwidth.
- If the available channel is a bandpass channel, we cannot send the digital signal directly to the channel; we need to convert the digital signal to an analog signal before transmission.



#### Transmission Impairment

Signals travel through transmission media, which are not perfect. The imperfection causes signal impairment. This means that the signal at the beginning of the medium is not the same as the signal at the end of the medium. What is sent is not what is received. Three causes of impairment are attenuation, distortion, and noise.


- Impairment causes
	- Attenuation
	- Distortion
	- Noise

#### Data Rate Limits

A very important consideration in data communications is how fast we can send data, in bits per second, over a channel. Data rate depends on three factors:
1. The bandwidth available
2. The level of the signals we use
3. The quality of the channel (the level of noise)


Noiseless Channel: Nyquist Bit Rate
Noisy Channel: Shannon Capacity

- Increasing the levels of a signal may reduce the reliability of the system.
- The Shannon capacity gives us the upper limit; the Nyquist formula tells us how many signal levels we need.


#### Performance


One important issue in networking is the performance of the network—how good is it? We discuss quality of service, an overall measurement of network performance, in greater detail in Chapter 24. In this section, we introduce terms that we need for future chapters.

- **Bandwidth** in hertz, refers to the range of frequencies in a composite signal or the range of frequencies that a channel can pass.
- **Bandwidth** in bits per second, refers to the speed of bit transmission in a channel or link.
- The bandwidth-delay product defines the number of bits that can fill the link.



### Analog-to-Digital




Analog-to-analog conversion is the representation of analog information by an analog signal. One may ask why we need to modulate an analog signal; it is already analog. Modulation is needed if the medium is bandpass in nature or if only a bandpass channel is available to us.


- Analog to digital conversion
	- amplitude modulation
	- frequency modulation
	- phase modulation


The total bandwidth required for AM can be determined from the bandwidth of the audio signal: B(AM) = 2B.

The total bandwidth required for FM can be determined from the bandwidth of the audio signal: B(FM) = 2(1 + β)B.


The total bandwidth required for PM can be determined from the bandwidth
and maximum amplitude of the modulating signal: B(PM) = 2(1 + β)B.



## Digital to Digital Conversion

- Types of conversion
	- Line coding
		- Unipolar --> NRZ
		- Polar --> NRZ, RZ and biphase (Manchester and different Manchester)
		- Bipolar --> AMI and pseudo ternary
		- Multilevel --> 2B/1Q, 8Q/6T and 4D-PAM5
		- Multitransition -> MLT-5
	- Block Coding
	- Scrambling
- Although the actual bandwidth of a digital signal is infinite, the effective bandwidth is finite.
- In NRZ-L the level of the voltage determines the value of the bit. In NRZ-I the inversion or the lack of inversion determines the value of the bit.
- NRZ-L and NRZ-I both have an average signal rate of N/2 Bd.
- NRZ-L and NRZ-I both have a DC component problem.
- In Manchester and differential Manchester encoding, the transition at the middle of the bit is used for synchronization.
- The minimum bandwidth of Manchester and differential Manchester is 2 times that of NRZ.
- In bipolar encoding, we use three levels: positive, zero, and negative.
- In mBnL schemes, a pattern of m data elements is encoded as a pattern of n signal elements in which 2^m ≤ L^n.
- Block coding is normally referred to as mB/nB coding; it replaces each m-bit group with an n-bit group.
- B8ZS substitutes eight consecutive zeros with 000VB0VB.
- HDB3 substitutes four consecutive zeros with 000V or B00V depending on the number of nonzero pulses after the last substitution.



## Analog to Digital Conversion


- There is two techniques
	- Pulse Code Modulation (PCM)
	- Delta Modulation (MD)
- According to the Nyquist theorem, the sampling rate must be at least 2 times the highest frequency contained in the signal.























