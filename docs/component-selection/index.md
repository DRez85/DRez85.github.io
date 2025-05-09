# Component Selection

## **Final Components Selected**
| Component               | Part Number         | Function                                          |
|-------------------------|---------------------|---------------------------------------------------|
| Microcontroller         | PIC18F47Q10         | Central control unit for UART, I2C, GPIO handling |
| H Bridge                | IFX9201SGAUMA1          | Controls Fan direction and speed      |
| Switching Regulator     | LM2575   | Converts barrel jack input to 3.3V regulated supply |
| Fan  | HA40101V4-1000U-A99       | 12V fan that is controlled by H brigde and microcontroller over SPI|

### **Microcontroller**

| Solution | Pros | Cons |
|----------|----------|----------|
| ![esp321N4](https://github.com/user-attachments/assets/8c6c63fb-29f0-4a42-845b-77c537fc106f) Solution 1<br> ESP32-S3-WROOM-1-N4<br> Cost: $2.95 Per Unit<br> [Link to Product](https://www.digikey.com/en/products/detail/espressif-systems/ESP32-S3-WROOM-1-N4/16162639)<br>| - Faster Processing for complex tasks<br>- Built in Wifi and Bluetooth 5 Connectivity<br>- Larger memory storage | - Higher Power Consumption<br>- Complex Peripheral Management<br>- Much more complex memory management |
|   ![PIC27](https://github.com/user-attachments/assets/1927a90f-8fa8-43db-8400-3ace6e7163e5) Solution 2<br> PIC18F27Q10-I/SO<br> Cost: $1.31 Per Unit<br> [Link to Product](https://www.digikey.com/en/products/detail/microchip-technology/PIC18F27Q10-I-SO/10064343)<br> | - Simple and easy architecture to program<br>- Multiple low power modes; overall low energy consumption<br>- More Reliable for wired standalone subsystems | - No built in wireless capabilities<br>- Fewer advanced I/O options<br>- Limited memory for advanced applications |
| ![PIC18LF46K22-I](https://github.com/user-attachments/assets/5f91bbba-034d-4f1c-8a3d-cd155d2a6a80) Solution 3<br> PIC18F47Q10T-I/MP<br> Cost: $3.85 Per Unit<br> [Link to Product](https://www.digikey.com/en/products/detail/microchip-technology/PIC18LF46K22-I-MV/2601555)<br>| - Faster Processing speed<br>- Adjustable GPIO pins<br>- 2 UART and 2 ICSP Pins | - Slower processing speeds<br>- No built in wifi or bluetooth modules<br>- Requires complex PCB design for high frequency operation |

**Choice:**  
Solution 2 - PIC18F27Q10-I/SO

**Rationale:**  
The PIC18F27Q10-I/SO offers an excellent balance of versatility, functionality, and efficient use of board space. With a rich array of bidirectional I/O pins that support both digital and analog functions, along with configurable peripherals such as timers, communication interfaces, and the Peripheral Pin Select (PPS) feature, this module provides the flexibility needed to handle complex tasks and interface with various sensors and actuators. Additionally, the integration of low-power features and dedicated programming interfaces makes it ideal for projects requiring robust performance in energy-sensitive environments. This combination of features in a compact package ensures that the design is both scalable and cost-effective, meeting the project's performance and connectivity requirements without unnecessary complexity.



### **Voltage Regulator**

| Solution | Pros | Cons |
|----------|----------|----------|
| ![LM2575](https://github.com/user-attachments/assets/f546c850-1c2c-41f9-b496-1d7d340e9a19) Solution 1<br> LM2575WU<br> Cost: $3.95 Per Unit<br> [Link to Product](https://www.digikey.com/en/products/detail/microchip-technology/LM2575WU/1027667)<br> | - High Efficiency<br>- High heat protection<br>- Prior use in class with through hole version | - Switch frequency make noise<br>- Limited Stock |
| ![VoltageMax5 5](https://github.com/user-attachments/assets/f8bbd664-95ab-4fe6-80ed-3f45c3ac1747) Solution 2<br> TPS75133QPWPR<br> Cost: $4.12 Per Unit<br> [Link to Product](https://www.digikey.com/en/products/detail/texas-instruments/TPS75133QPWPR/1673042)<br> | - High Efficiency<br>- High Temperature Range | - Switch frequency make noise<br>- Low dropout Voltage<br>- 5.5 V Max Input |
| ![LM1085ISX](https://github.com/user-attachments/assets/6600a851-bbd8-4a5b-86d0-18e0372d0d5f) Solution 3<br> LM1085ISX-3.3/NOPB<br> Cost: $1.84 Per Unit<br> [Link to Product](https://www.digikey.com/en/products/detail/nisshinbo-micro-devices-inc/RP509Z001D-E2-F/10217681)<br> | - Larger Package Size<br> - Wide Voltage Input Range | - High dropout voltage |

**Choice:**  
Solution 1 - LM2575WU

**Rationale:**  
The LM2575WU was chosen as our voltage regulator due to its efficiency, reliability, and ease of integration in our power management system. As a step-down (buck) switching regulator, it efficiently converts higher input voltages, such as 9V, to a stable 3.3V output, ensuring optimal power delivery while minimizing heat dissipation compared to traditional linear regulators. With a wide input voltage range (4V to 40V) and a 1A output current capacity, it provides flexibility for various power sources and load conditions. Its internal frequency compensation, fixed 52kHz switching frequency, and minimal external component requirements simplify circuit design and reduce PCB space. Additionally, the integrated thermal shutdown and current limit protection enhance system safety and durability. Given our prior experience and familiarity with this regulator, its selection ensures a seamless and efficient voltage regulation solution for our project.

### **Motor Driver**

| Solution | Pros | Cons |
|----------|----------|----------|
| ![NCV7708FDWR2G](https://github.com/user-attachments/assets/e3d613c3-ad3f-4f2f-a713-1b056073b67e) Solution 1<br> NCV7708FDWR2G<br>  Cost: $ 4.36 per Unit<br> [Link to Product](https://www.digikey.com/en/products/detail/onsemi/NCV7708FDWR2G/9829237)<br> | - Readily available<br> - Fully integrated control and power.<br> | -Expensive <br> - 28 Pins may be difficult to solder. 
| ![IFX9201SGAUMA1](https://github.com/user-attachments/assets/a3cdcdeb-12d7-4e11-9d38-53d74f1c8f19) Solution 2<br> IFX9201SGAUMA1<br> Cost $ 3.68 per unit<br> [Link to Product](https://www.digikey.com/en/products/detail/infineon-technologies/ifx9201sgauma1/5415542)<br> | - Familiarity used in lab in class.<br> - Uses SPI communication<br> | - Difficult to program
 
## **PIC18F27Q10 Information Table**
| PIC18F27Q10 Info| Answer | Comments |
|----------|----------|----------|
| Model   | PIC18F27Q10-I/SO   |    |
| Product Page URL   | [MircoChip](https://www.microchip.com/en-us/product/PIC18F27Q10)  |    |
| PIC18F27Q10-I/SO Datasheet URL  | [Datasheet](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ProductDocuments/DataSheets/PIC18F27-47Q10-Micorcontroller-Data-Sheet-DS40002043.pdf)   | Found on Microchip.com   |
| PIC18F27Q10-I/SO supplemental data sheet   | [Datasheet](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ApplicationNotes/ApplicationNotes/Getting-Started-with-UART-Using-EUSART-on-PIC18-90003282A.pdf)   | Has more details on using Uart   |
|  PIC18F27Q10-I/SO supplemental data sheet  | [Datasheet](https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ApplicationNotes/ApplicationNotes/Getting-Started-With-SPI-Using-MSSP-on-PIC18-90003265B.pdf)   | Has details on using SPI for debugging   |
| PIC18F27Q10-I/SO supplemental data sheet  | [Datasheet](https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ApplicationNotes/ApplicationNotes/90003130A.pdf)   | Has details on chaning GPIO function   |
| Vendor Link   | [Digikey](https://www.digikey.com/en/products/detail/microchip-technology/PIC18F27Q10-I-SO/10064343)   |   |
| Code Examples   | [Link](https://mplabxpress.microchip.com/mplabcloud/example?device=q10)  | All Code Examples   |
| Unit Cost   | $1.31   |    |
| Absolute Maximum Current for entire IC  | 200mA   | as found in datasheet   |
| Supply Voltage Range  | 1.8V / 3.3V / 5.5V   | Min/Nominal/ Max, as found in datasheet  |
| Maximum GPIO current(per pin)  | 25mA   | as found in datasheet  |
|Supports External Interrupts?  | Yes   | as found in datasheet   |
|Required Programming Hardware, Cost, URL |  [Link](https://www.microchip.com/)  | as found in datasheet   |

### **Associated Pins**

| Peripheral        | Availability  | Associated Pins                          |
|------------------|--------------|------------------------------------------|
| **UART Modules**  | 2 modules    | Pins 17 (TX1), 18 (RX1), 27 (TX2), 28 (RX2) |
| **SPI Modules**   | 2 modules    | Pins 14 (SCK1), 15 (SDI1), 16 (SDO1), 21 (SS2), 22 (SCK2), 23 (SDI2), 24 (SDO2), 26 (SS1) |
| **I2C Modules**   | 2 modules    | Pins 14 (SCL1), 15 (SDA1), 22 (SCL2), 23 (SDA2) |
| **GPIO Pins**     | 25 pins      | Pins 2-7, 9-13, 17-28                     |
| **ADC Channels**  | 10 channels  | Pins 2-7, 13, 25, 26, 27                 |
| **PWM Outputs**   | 3 outputs    | Pins 6, 7, 13                            |
| **Power (VDD/GND)** | 2 VDD, 2 GND | Pins 8 (GND), 19 (GND), 20 (VDD), 28 (VDD) |

### **Datasheet References**

![28pindiagram](https://github.com/user-attachments/assets/e29e0a40-a9e7-43e8-8b9e-00141c12342f)

![28pintable](https://github.com/user-attachments/assets/ab2ad464-3020-47bc-9b73-5c998b1a7fe6)

![28pintable2](https://github.com/user-attachments/assets/8ec3cdc5-3d69-4768-a943-f933c83dd7df)


