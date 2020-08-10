# 2-1 Overview of the Physical Layer - PEARSON

#### Scope of the physical layer

* How we use **analog signals** to send **digital bits**

  ![Screen Shot 2020-08-10 at 12.42.33 pm](/Users/annacheng/Library/Application Support/typora-user-images/Screen Shot 2020-08-10 at 12.42.33 pm.png)

#### Topics

1. Properties of media
   - wires, fiber optics, wireless

2. SImple signal propagation
   * Bandwidth, attenuation, noise
3. Modulation schemes
   * Representing bits, noise
4. Fundamental limits
   * Nyquist, Shannon

---

#### Simple Link Model

* An abstraction of a physical channel

  * Rate (or bandwidth, capacity, speed) in bits/second

  * Delay in seconds, related to length

    ![Screen Shot 2020-08-10 at 12.44.26 pm](/Users/annacheng/Library/Application Support/typora-user-images/Screen Shot 2020-08-10 at 12.44.26 pm.png)

* Other important properties

  * Whether the channel ? broadcast
  * ? its error rate

---

#### Mesage latency

* Latency is the **delay** to send a message over a link

  * [Transmission delay](https://en.wikipedia.org/wiki/Transmission_delay): time to put N-bit message "on the wire"
    * D = N/R seconds
    * D is the transmission delay in seconds
    * N is the number of bits
    * R is the rate of transmission (say in bits per second)
  * [Propagation delay]([https://en.wikipedia.org/wiki/Propagation_delay#:~:text=In%20computer%20networks%2C%20propagation%20delay,the%20sender%20to%20the%20receiver.&text=Propagation%20delay%20is%20equal%20to,i.e.%20the%20speed%20of%20light.](https://en.wikipedia.org/wiki/Propagation_delay#:~:text=In computer networks%2C propagation delay,the sender to the receiver.&text=Propagation delay is equal to,i.e. the speed of light.)): time for bits to propagate across the wire
    * Length / (2/3 s) = D
    * s = c (i.e the speed of light)
    * Propagation delay is equal to *d / s* where *d* is the distance and *s* is the [wave propagation speed](https://en.wikipedia.org/wiki/Wave_propagation_speed).

  * Combining the two terms we have
    * L = M/R + D

##### Metric Units

| Prefix | Exp.   | prefix   | exp.      |
| ------ | ------ | -------- | --------- |
| K(ilo) | $10^3$ | m(illi)  | $10^{-3}$ |
| M(ega) | $10^6$ | μ(micro) | $10^{-6}$ |
| G(iga) | $10^9$ | N(ano)   | $10^{-9}$ |

* Use powers of 10 for rates, 2 for storage
  * 1 Mbps = 1,000,000 bps, 1 KB = $2^{10}$ bytes = 1024 bits
* "B" is for bytes, "b" is for bits

##### Latency Examples

* "Dialup" with a telephone modem

  * D = 5 ms, R = 56 kbps, M = 1250 bytes

    * L = M/R + D

    * L = 5 ms + (1250)(8)/(56)($10^3$) sec 

      = 184 ms

* Broadband cross-country link

  * D = 50 ms, R =10 Mbps, M = 1250 bytes

    * L = M/R + D

    * L = 50 ms + (1250)(8) / (10)($16^6$) sec 

      = 51 ms

* A long link or a slow rate means high latency

  * Often, one delay component dominates

---

#### Bandwidth-Delay Product

* Messages take space on the wire! 

  ![Screen Shot 2020-08-10 at 12.25.34 pm](/Users/annacheng/Library/Application Support/typora-user-images/Screen Shot 2020-08-10 at 12.25.34 pm.png)

  

* The amount of data in flight is the bandwidth-delay (BD) product

  * BD = R X D
  * Measure in bits, or in messages
  * Small for LANs, big for "long fat" pipes

##### Bandwidth-Delay Example

* Fiber at home, cross-country R = 40 Mbps, D = 50 ms

  * BD = (40)($10^6$) X (50)($10^{-3}$) bits

    = 2000 Kbit

    = 250 KB

* That's quite a lot of data "in the network"!

