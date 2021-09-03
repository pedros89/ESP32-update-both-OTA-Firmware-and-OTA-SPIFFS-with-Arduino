# ESP32-update-both-OTA-Firmware-and-OTA-SPIFFS-with-Arduino
Load this code on your EPS32 to OTA update ESP32 APP and SPIFFS partition

- Generate the Bin File. Arduino → sketch → export compiled sketch

- Place the `.bin` images on your hosting server

- for the process on how to generate SPIFFS images follow this link
[ESP32-OTA-update-SPIFFS-with-Arduino](https://github.com/pedros89/ESP32-OTA-update-SPIFFS-with-Arduino)

This piece of code is particularly important, where the config for the HTTPS connection takes place.
Make sure you format your certificate correctly like you find in the file `CertMeren.h`
```
  esp_http_client_config_t config;
      memset(&config, 0, sizeof(esp_http_client_config_t));
      config.url = FIRMWARE_URL;
      config.cert_pem = UPGRADE_SERVER_CERT;
      
```
