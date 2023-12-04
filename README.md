# Advanced RMT Transmit & Receive Example -- Simulate 1-Wire Bus

Connection :

```plain
┌──────────────────────────┐
│                      3.3V├───────┬─────────────┬──────────────────────┐
│                          │      ┌┴┐            │VDD                   │VDD
│          ESP Board       │  4.7k│ │     ┌──────┴──────┐        ┌──────┴──────┐
│                          │      └┬┘   DQ│             │      DQ│             │
│          ONEWIRE_GPIO_PIN├───────┴──┬───┤   DS18B20   │    ┌───┤   DS18B20   │   ......
│                          │          └───│-------------│────┴───│-------------│──
│                          │              └──────┬──────┘        └──────┬──────┘
│                          │                     │GND                   │GND
│                       GND├─────────────────────┴──────────────────────┘
└──────────────────────────┘
```
Example:
![зображення](https://github.com/dania93/TemperatureMeasurementByDS18B20/assets/41265108/0ce9e467-2ec5-48d7-9a55-c9e61592d6df)

The GPIO number used in this example can be changed according to your board, by the macro `EXAMPLE_ONEWIRE_BUS_GPIO` defined in [onewire_example_main.c](main/onewire_example_main.c).

See the [Getting Started Guide](https://docs.espressif.com/projects/esp-idf/en/latest/get-started/index.html) for full steps to configure and use ESP-IDF to build projects.

## Console Output

```plain
I (340) main_task: Started on CPU0
I (350) main_task: Calling app_main()
I (350) gpio: GPIO[0]| InputEn: 1| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0
I (360) gpio: GPIO[0]| InputEn: 1| OutputEn: 1| OpenDrain: 1| Pullup: 1| Pulldown: 0| Intr:0
I (370) example: 1-Wire bus installed on GPIO0
I (370) example: Device iterator created, start searching...
I (490) example: Found a DS18B20[0], address: 070822502019FC28
I (590) example: Found a DS18B20[1], address: FC0921C076034628
I (590) example: Searching done, 2 DS18B20 device(s) found
I (1620) example: temperature read from DS18B20[0]: 22.50C
I (2430) example: temperature read from DS18B20[1]: 22.81C
I (3440) example: temperature read from DS18B20[0]: 22.50C
I (4250) example: temperature read from DS18B20[1]: 22.81C
I (5260) example: temperature read from DS18B20[0]: 22.50C
I (6070) example: temperature read from DS18B20[1]: 22.81C
```

Example:

![зображення](https://github.com/dania93/TemperatureMeasurementByDS18B20/assets/41265108/857962a4-3d46-4286-9139-4920b852a6e7)


## Troubleshooting

For any technical queries, please open an [issue](https://github.com/espressif/esp-idf/issues) on GitHub. We will get back to you soon.
