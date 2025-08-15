# REAL-TIME-VECHILE-STATUS-MONITORING-USING-CAN
The aim of the project is to enhance vehicle safety and monitoring by using Controller Area Network (CAN) protocol. This system is designed to display critical vehicle parameters such as fuel percentage, indicator status, and airbag status/activation in real time.
________________________________________________________________________________________________________________________________________
**Real Time Vehicle Status Monitoring Using CAN Protocol**

**Overview**
Here’s a **more concise, visually organized, and reader-friendly overview** of the same content, suitable for a **project brief** or **executive summary**:

---

Real-Time Vehicle Status Monitoring (CAN-Based)

 **Overview**

A modular, CAN-bus-based embedded system that **monitors and shares vehicle status** across different ECUs in real time.
It ensures **fast, reliable** communication for critical parameters such as **fuel level, indicator status, and airbag alerts**.

---

 **Core Functions**

* **Fuel Monitoring** → Reads fuel percentage via ADC, transmits over CAN.
* **Indicator Control** → Handles Left/Right indicator status & hazard alerts.
* **Airbag Detection** → Detects sudden impacts using MMA7660 accelerometer and sends deployment alerts.

---
By utilizing CAN communication, this system provides reliable and efficient data transfer between different ECUs (Electronic Control Units) in a vehicle.

 **Key Features**

 **Standardized CAN Communication** – Robust inter-ECU data transfer
 
 **Real-Time Updates** – Instant sensor-to-display feedback
 
 **Dynamic Parameter Display** – LCD + Serial output
 
 **Scalable & Modular** – Easy integration of new sensors or nodes
 
**Supports Simulation & Real Hardware** – Works in Proteus and on actual LPC2129 boards

---


 **System Nodes**


 **Main Node**       Airbag detection (MMA7660), central display, CAN relay 
 
 **Fuel Node**       Fuel percentage measurement via ADC, CAN transmission 
 
 **Indicator Node**  Indicator light control & status broadcast over CAN    

---

 **Hardware Components**

* **Controller**: LPC2129 ARM7 microcontroller
* **Transceiver**: MCP2551 / SN65HVD230
* **Display**: 16x2 LCD
* **Sensors**: MMA7660 (acceleration), Fuel level sensor (ADC)
* **Inputs**: Push buttons / toggle switches (EINT0, EINT1 for indicators)

---

 **Software Tools**

* **Language**: C / C++
* **IDE**: Keil µVision (for ARM7)
* **Libraries**: CAN protocol stack, ADC, LCD, I2C drivers
* **Debugging**: Serial terminal (UART)
* **Simulation**: Proteus (optional)

---

 **Project Structure**
 
/src

├── main_node.c

├── fuel_node.c

├── indicator_node.c

├── lcd.c

├── lcd_defines.h

├── can.c

├── can.h

├── can_defines.h

├── adc.c

├── adc_defines.h

├── interrupt.h

├── types.h

├── uart_tx.c

└── uart_defines.h

**Usages of the System Data**

1.** Driver Information Display**

1.Shows real-time fuel level, indicator status, and airbag alerts on the dashboard LCD or infotainment screen.

2.Helps the driver make informed decisions (e.g., refuel before running out).

2.** Safety Alerts**

1.Immediate airbag deployment alerts can trigger:

2.Audible alarms

3.Hazard light activation

4.Transmission of emergency data to other ECUs or connected devices

3. **Maintenance & Diagnostics**
   
1.Mechanics can access CAN messages to check:

2.Fuel sensor health

3.Indicator functionality

4.Accelerometer status

5.Reduces troubleshooting time by providing direct sensor readings.


