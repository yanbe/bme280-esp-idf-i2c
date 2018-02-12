Sample code for reading values from a BME280 via ESP-IDF's I2C master driver
====================

See main code main.c_.

----------
About
----------

This sample code implement procedures to read values from BME280 sensor (pressure, temperature, humidity) via ESP-IDF's I2C master driver. It supports both normal mode and forced mode described in `Bosch's BME280 datasheet`_, Section 3.3 Sensor modes, Page 12.

This code is not compatible with the newest Bosch driver version. The last version that works correctly is v2.0.5, commit cf40d00_.

----------
For local setup
----------

For your local setup, connect SDI pin to GPIO 15 pin and the SCK to GPIO 2 pin as they are default ports (I2C_SDA, I2C_SCL) for I2C master according to `ESP32 datasheet`_, C.4. IO_MUX, Page 49.

Don't forget to connect SDO to Vio too. It maps device address to 0x77 (not 0x76). This is default setup for BME280 I2C as described in `Bosch's BME280 datasheet`_, Section 6.2 I2C Interface, Page 31.

.. _main.c: https://github.com/yanbe/bme280-esp-idf-i2c/blob/master/main/main.c
.. _ESP32 datasheet: https://www.espressif.com/sites/default/files/documentation/esp32_datasheet_en.pdf
.. _Bosch's BME280 datasheet: https://ae-bst.resource.bosch.com/media/_tech/media/datasheets/BST-BME280_DS001-11.pdf
.. _cf40d00: https://github.com/BoschSensortec/BME280_driver/tree/cf40d00b0b5139e287b670881c433c0041d98d9f
