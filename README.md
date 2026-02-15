# system-diagram

Long-distance friendships often suffer from "communication decay." Kompanion is an interactive desktop installation that uses a living SCOBY (Symbiotic Culture of Bacteria and Yeast) as a physical metaphor for long-distance friendship. It addresses this by providing a shared, low-maintenance responsibility. 

When User A and User B are both present in front of the device, it will transmit signals to each other's physical devices, which triggers the light to emit a warm glow, showing presence. Whenever the other SCOBY is in need of nutrients (measured by temperature and pH level sensors), User A's device light will glow red, reminding them to tap on their device to feed User B's SCOBY:
1. Presence Sync (The "Warm Glow")
Using sensors, the device detects when a user is physically near.
Interaction: When both User A and User B are "present" simultaneously, both devices emit a synchronized warm amber glow. This creates a sense of "passive togetherness," simulating the feeling of being in the same room without needing to call.

2. Biological SOS (The "Red Reminder")
The device monitors the SCOBY's environment using pH and temperature sensors.
Interaction: If User B’s SCOBY becomes unhealthy (pH too high or temp too low), User A’s device glows red. User A is notified that their friend's "biological avatar" needs care. User A then taps their device to remotely trigger a nutrient "boost" for User B.

Potential  Flow
1. User B’s SCOBY is low on pH
2. Device B sends a "Critical Health" alert via MQTT
3. Device A glows Red, signaling User A
4. User A taps the device
5. Device A sends a "Feed" command back to Device B
6. Device B’s pump activates, delivering sugar water

Hardware Requirements
Microcontroller: ESP32 (for Wi-Fi capability)
Actuators: 5V Submersible Water Pump or Peristaltic Pump
Lighting: WS2812B (NeoPixel) LED Ring
Power: 9V Battery or 5V DC Wall Adapter
Sensors: HC-SR04 Ultrasonic Sensor (for presence detection)
Analog pH Meter Kit: For biological monitoring
DS18B20 Waterproof Temp Sensor: To ensure SCOBY stability
Biological: SCOBY starter culture, black tea, and cane sugar

Future Implementation
- Automatically triggers "hunger" lights if friends haven't spoken in a set number of days
- Using heart-rate sensors to pulse the LED ring in sync with the distant friend
