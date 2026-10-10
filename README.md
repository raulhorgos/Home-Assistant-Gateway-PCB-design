# Home Assistant Gateway PCB design 
This repository contains the hardware design files for the TIE 2025 Home Assistant Gateway project, as detailed in the reference document 
"TIE 2025-R2_SCH.PDF". 
The gateway is designed to act as the central brain of a smart home, bridging communication between devices and automating routines. 
It enables the control of smart lights, thermostats, and appliances while integrating communication protocols like Wi-Fi, Zigbee, 
and Bluetooth. 
The hardware provides secure remote access and supports AI-enhanced personalized assistance.
   
Hardware Specifications

Core Processor: 

The system is driven by a Microchip SAMA7G54 System-in-Package. 
The design specifically utilizes the SAMA7G54D2G-I/4UB variant.   
Power Management: 	An MCP16501 PMIC regulates the system power. 
			The PMIC converts a main 5V input into multiple necessary power rails, including VDD_3V3, VDDCORE, and VDDIODDR. 
  
Networking: High-speed network connectivity is provided by a Microchip LAN8840 Gigabit Ethernet transceiver.
   
USB Connectivity: 
Peripheral connections are supported by a USB Type-C device connector and a USB Type-A host connector. 
The system's power traces are designed to support up to 5A on the USB power planes. 
  
Camera Integration: A 15-pin FPC connector provides a MIPI-CSI interface for connecting camera modules.
   
Storage & Interface: The board includes an SD Card connector for external data storage. 

Physical user interactions are supported by an RGB LED and two push-buttons mapped to nSTART and NRST functions.   
Debugging: A UART Debug Connector (DBGU) provides serial access for development and testing.   
The Altium Designer printed circuit board requires specific layout parameters, including 50-ohm impedances for single-ended traces and 
90-ohm to 100-ohm impedances for differential pairs. The routing also enforces strict length-matching tolerances for high-speed interfaces
 like the SD Card data lines and the MIPI-CSI camera connections.