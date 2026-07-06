#Auto-Disconnect Smart Charger using ESP8266

This project is designed to automatically disconnect a charging circuit when the charging current falls below a preset value. The main objective is to avoid unnecessary power consumption after the charging process is complete by monitoring the charging current instead of relying on a fixed charging time.

To demonstrate the concept safely, a capacitor is used as the charging load instead of a mobile phone battery. As a capacitor charges, the charging current naturally decreases and eventually becomes very small. This behavior makes it a simple and safe way to test the automatic cutoff mechanism without using an actual battery.

The system is built around the ESP8266 (NodeMCU), which continuously monitors the charging current using an INA219 current sensor. When the measured current drops below the predefined threshold, the ESP8266 turns off a USB relay module, disconnecting the power supply automatically. This shows how current-based charging control can be implemented in an embedded system.

#Features
- Automatically disconnects the charging circuit when the charging current reaches the set threshold.
- Continuously monitors charging current using the INA219 sensor.
- Controls power supply through a USB relay module.
- Built using the ESP8266, making it easy to extend for future IoT applications.
- Uses a capacitor as the charging load for safe and reliable testing.
- Demonstrates a simple approach to energy-efficient charging automation.
  
#Hardware Components
- ESP8266 (NodeMCU)
- INA219 Current and Voltage Sensor
- USB Relay Module
- Capacitor (used as the charging load)
- DC Power Supply
- Breadboard and Connecting Wires
  
#Working

When the charging process begins, the ESP8266 continuously reads the current measured by the INA219 sensor. Initially, the charging current is relatively high, but as the capacitor becomes fully charged, the current gradually decreases. Once the current falls below the predefined threshold, the ESP8266 switches off the relay, cutting off the power supply to the charging circuit automatically.

This project demonstrates a simple yet effective method of implementing automatic charging cutoff based on real-time current monitoring, making it a useful concept for smart charging and energy-saving applications.
