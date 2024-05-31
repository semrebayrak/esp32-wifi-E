```markdown
# ESP32 Wi-Fi Configuration

This project provides a Wi-Fi configuration system for ESP32 devices. The ESP32 starts in Access Point (AP) mode, allowing users to connect and input Wi-Fi credentials through a web interface. Once the credentials are received, the ESP32 switches to Station (STA) mode to connect to the specified Wi-Fi network.

## Features

- **AP Mode:** ESP32 starts in AP mode for Wi-Fi configuration.
- **STA Mode:** Switches to STA mode to connect to the specified network after receiving credentials.
- **Web Server:** Built-in web server for setting Wi-Fi credentials.
- **NVS Storage:** Securely store Wi-Fi credentials in Non-Volatile Storage (NVS).

## Getting Started

### Prerequisites

- ESP32 development board
- ESP-IDF development environment
- Serial terminal application (e.g., minicom, PuTTY)

### Installation

1. **Clone the Repository**

   ```sh
   git clone https://github.com/yourusername/esp32-wifi-switch.git
   cd esp32-wifi-switch
   ```

2. **Set up ESP-IDF**

   Follow the instructions on the [ESP-IDF Getting Started Guide](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/index.html) to set up your development environment.

3. **Build and Flash the Firmware**

   ```sh
   idf.py set-target esp32
   idf.py build
   idf.py flash
   ```

4. **Monitor the Serial Output**

   ```sh
   idf.py monitor
   ```

### Usage

1. **Connect to the ESP32 AP**

   Connect your device to the Wi-Fi network named `ESP32_Config`.

2. **Access the Configuration Portal**

   Open a web browser and navigate to `http://192.168.4.1`. You will see a form where you can input the SSID and password of your desired Wi-Fi network.

3. **Submit the Form**

   Enter the SSID and password, then click "Set Wi-Fi". The ESP32 will save the credentials, restart, and attempt to connect to the specified network in STA mode.

### Code Overview

- **main.c:** Entry point of the application, initializes NVS, starts the web server, and configures Wi-Fi.
- **wifi.c:** Contains Wi-Fi initialization and event handling logic.

### Troubleshooting

- **Cannot Connect to AP:** Ensure your device is within range and the AP mode is correctly configured.
- **Wi-Fi Credentials Not Saved:** Check the serial output for errors and ensure NVS is properly initialized.

### Contributing

Contributions are welcome! Please open an issue or submit a pull request.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Acknowledgments

- [Espressif Systems](https://www.espressif.com/) for their excellent ESP32 hardware and software tools.
- The [ESP-IDF community](https://github.com/espressif/esp-idf) for their support and contributions.
```
