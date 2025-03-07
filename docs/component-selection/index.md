# Component Selection


### **Microcontroller**

| Solution | Pros | Cons |
|----------|----------|----------|
| ![esp321N4](https://github.com/user-attachments/assets/8c6c63fb-29f0-4a42-845b-77c537fc106f) Solution 1<br> ESP32-S3-WROOM-1-N4<br> Cost: $2.95 Per Unit<br> [Link to Product](https://www.digikey.com/en/products/detail/espressif-systems/ESP32-S3-WROOM-1-N4/16162639)<br>| - Faster Processing for complex tasks<br>- Built in Wifi and Bluetooth 5 Connectivity<br>- Larger memory storage | - Higher Power Consumption<br>- Complex Peripheral Management<br>- Much more complex memory management |
|   ![PIC27](https://github.com/user-attachments/assets/1927a90f-8fa8-43db-8400-3ace6e7163e5) Solution 2<br> PIC18F27Q10-I/SO<br> Cost: $1.31 Per Unit<br> [Link to Product](https://www.digikey.com/en/products/detail/microchip-technology/PIC18F27Q10-I-SO/10064343)<br> | - Simple and easy architecture to program<br>- Multiple low power modes; overall low energy consumption<br>- More Reliable for wired standalone subsystems | - No built in wireless capabilities<br>- Fewer advanced I/O options<br>- Limited memory for advanced applications |
| ![Alternatepic](https://github.com/user-attachments/assets/f7c9fc8d-b4b8-443e-97ce-a1c4e1f9f043) Solution 3<br> PIC18F47Q10T-I/MP<br> Cost: $1.74 Per Unit<br> [Link to Product](https://www.digikey.com/en/products/detail/microchip-technology/PIC18F47Q10T-I-MP/10187787?s=N4IgTCBcDaIAoEkDCBGAHAMQCwHYCKKADACoC0CA9ALJwgC6AvkA)<br>| - Faster Processing speed<br>- Adjustable GPIO pins<br>- 2 UART and 2 ICSP Pins | - Slower processing speeds<br>- No built in wifi or bluetooth modules<br>- Requires complex PCB design for high frequency operation |

**Choice:**  
Solution 2 - PIC18F27Q10-I/SO

**Rationale:**  
The PIC18F27Q10-I/SO offers an excellent balance of versatility, functionality, and efficient use of board space. With a rich array of bidirectional I/O pins that support both digital and analog functions, along with configurable peripherals such as timers, communication interfaces, and the Peripheral Pin Select (PPS) feature, this module provides the flexibility needed to handle complex tasks and interface with various sensors and actuators. Additionally, the integration of low-power features and dedicated programming interfaces makes it ideal for projects requiring robust performance in energy-sensitive environments. This combination of features in a compact package ensures that the design is both scalable and cost-effective, meeting the project's performance and connectivity requirements without unnecessary complexity.



### **Voltage Regulator**

| Solution | Pros | Cons |
|----------|----------|----------|
| ![LM2575](https://github.com/user-attachments/assets/f546c850-1c2c-41f9-b496-1d7d340e9a19) Solution 1<br> LM2575WU<br> Cost: $3.95 Per Unit<br> [Link to Product](https://www.digikey.com/en/products/detail/microchip-technology/LM2575WU/1027667)<br> | - High Efficiency<br>- High heat protection<br>- Prior use in class with through hole version | - Switch frequency make noise<br>- Limited Stock |
| ![VoltageMax5 5](https://github.com/user-attachments/assets/f8bbd664-95ab-4fe6-80ed-3f45c3ac1747) Solution 2<br> TPS75133QPWPR<br> Cost: $4.12 Per Unit<br> [Link to Product](https://www.digikey.com/en/products/detail/texas-instruments/TPS75133QPWPR/1673042)<br> | - High Efficiency<br>- High Temperature Range | - Switch frequency make noise<br>- Low dropout Voltage<br>- 5.5 V Max Input |
| ![Voltagesolder](https://github.com/user-attachments/assets/7f30f434-51ad-4147-a66e-904c9023636f) Solution 3<br> RP509Z001D-E2-F<br> Cost: $0.70 Per Unit<br> [Link to Product](https://www.digikey.com/en/products/detail/nisshinbo-micro-devices-inc/RP509Z001D-E2-F/10217681)<br>| - High Efficiency<br>- Very Inexpensive | - Very Difficult Soldering<br>- Low max Temp<br>- 6.5 V Max Input |

**Choice:**  
Solution 1 - LM2575WU 

**Rationale:**  
The LM2575WU was chosen as our voltage regulator due to its efficiency, reliability, and ease of integration in our power management system. As a step-down (buck) switching regulator, it efficiently converts higher input voltages, such as 9V, to a stable 3.3V output, ensuring optimal power delivery while minimizing heat dissipation compared to traditional linear regulators. With a wide input voltage range (4V to 40V) and a 1A output current capacity, it provides flexibility for various power sources and load conditions. Its internal frequency compensation, fixed 52kHz switching frequency, and minimal external component requirements simplify circuit design and reduce PCB space. Additionally, the integrated thermal shutdown and current limit protection enhance system safety and durability. Given our prior experience and familiarity with this regulator, its selection ensures a seamless and efficient voltage regulation solution for our project.
