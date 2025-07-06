## Uardecs\_ESP32
[日本語版はこちら](https://github.com/andotoecno/UARDECS_ESP32/blob/main/README_jp.md)
  - This is a library that ports [UARDECS](https://uecs.org/arduino/uardecs.html) to be used with the ESP32's WiFi. It can be used in the same way as the original UARDECS.
      - The `main` branch contains a port of the Arduino Uno version, and a port of the Mega version is being tested on the `feature/mega-imigration` branch.
  - The following operations have been confirmed:
      - Viewing node settings from a browser and updating IP addresses, etc.
      - Confirming UDP packet reception with the UECS Packet Send/Receive Support Tool.
      - Confirming reception of test data with UECS-GEAR.
      - Confirming reception with UECS-Pi and Arsprout Pi.
  - For implementation details and porting notes, please refer to [README\_dev.md](https://www.google.com/search?q=README_dev.md).

## License

  - This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
  - See [LICENSE](https://www.google.com/search?q=LICENSE) for more details.
