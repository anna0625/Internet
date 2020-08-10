# Analysis Using Wireshark

#### OSI Model - An ideal networking design

* similar to Internet

![Screen Shot 2020-08-10 at 1.13.55 pm](/Users/annacheng/Library/Application Support/typora-user-images/Screen Shot 2020-08-10 at 1.13.55 pm.png)

* Layering leads to Encapsulation

  * frame check sequence (FCS)
  * protocals are the same in encapsulation and decapsulation 

  ![Screen Shot 2020-08-10 at 1.16.18 pm](/Users/annacheng/Library/Application Support/typora-user-images/Screen Shot 2020-08-10 at 1.16.18 pm.png)

* Decapsulation

  ![Screen Shot 2020-08-10 at 1.19.22 pm](/Users/annacheng/Library/Application Support/typora-user-images/Screen Shot 2020-08-10 at 1.19.22 pm.png)

* How exactly does this transmission take place through the network?

  * ?

* Addresses

  * IP address (Network Layer)
    * Helps route information from one network to another
    * Can be static or dynamic
    * Format (logical addressing)
      * IPV4 102.50.4.5
      * IPV6

  * MAC Address (Data Link Layer)
    * Helps identify specific devices from a multitude of devices out there
    * It is unique for each device
    * Format (physical addressing)
      * E8:FC:AF:B9:BE:A2 (one of them..)

---

#### Transmission Control Protocol (TCP)

* Transport layer

* Connection-oriented 
  * towards transmission of data between two devices
* Ensures reliability
  * through re-transmission of lost/corrupted data

* 3 Way Handshake

  * SYN - sync message

  ![Screen Shot 2020-08-10 at 1.37.05 pm](/Users/annacheng/Library/Application Support/typora-user-images/Screen Shot 2020-08-10 at 1.37.05 pm.png)

---

#### User Datagram Protocol

* Connection-less approach
  * towards transmission of data between two devices
* Noreliability
  * best effot basis of transmission

* Wireshark
  * packet capture and analysis tool
  * GUI for packet analysis
  * live packet or review previously captured data

