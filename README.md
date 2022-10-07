# Hello World Example

This is based on the [standard Hello world]() from the ESP-IDF examples, and the
[u8g2-hal-esp-idf i2c test
file](https://github.com/mkfrey/u8g2-hal-esp-idf/blob/master/examples/test_SSD1306_i2c.c)

Prints "Hello World" onto a 0.91" 128x32 SSD1306 OLED display. If you wish to
use this project with a different display, select the u8g2 setup function
(`u8g2_Setup_ssd1306_i2c_128x32_univision_f` in the example code) according to
the [u8g2 wiki](https://github.com/olikraus/u8g2/wiki/u8g2setupcpp)

## How to use example

Follow detailed instructions provided specifically for this example. however,
in the [Step 5: Start a project](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/index.html#step-5-start-a-project)
clone this project and it's submodules with:

```bash
git clone https://github.com/jdthorpe/esp-idf-u8g2-hello-world
cd esp-idf-u8g2-hello-world
git submodule update --init --recursive
```

Select the instructions depending on Espressif chip installed on your development board:

- [ESP32 Getting Started Guide](https://docs.espressif.com/projects/esp-idf/en/stable/get-started/index.html)
- [ESP32-S2 Getting Started Guide](https://docs.espressif.com/projects/esp-idf/en/latest/esp32s2/get-started/index.html)

## Example folder contents

The project **hello_world** contains one source file in C++ language
[hello_world_main.cpp](main/hello_world_main.cpp). The file is located in folder
[main](main).

If you prefer to use C instead of C++, change the extension of the main file to
`.c`, and replace the `extern "C"` block in main `#include <u8g2_esp32_hal.h>`

ESP-IDF projects are built using CMake. The project build configuration is
contained in `CMakeLists.txt` files that provide set of directives and
instructions describing the project's source files and targets (executable,
library, or both).

Below is short explanation of remaining files in the project folder.

```
├── CMakeLists.txt
├── main
│   ├── CMakeLists.txt
│   ├── component.mk           Component make file
│   └── hello_world_main.cpp
├── Makefile                   Makefile used by legacy GNU Make
└── README.md                  This is the file you are currently reading
```

For more information on structure and contents of ESP-IDF projects, please refer to Section [Build System](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-guides/build-system.html) of the ESP-IDF Programming Guide.

## Troubleshooting

- Program upload failure

  - Hardware connection is not correct: run `idf.py -p PORT monitor`, and reboot your board to see if there are any output logs.
  - The baud rate for downloading is too high: lower your baud rate in the `menuconfig` menu, and try again.

## Technical support and feedback

Please use the following feedback channels:

- For technical queries, go to the [esp32.com](https://esp32.com/) forum
- For a feature request or bug report, create a [GitHub issue](https://github.com/espressif/esp-idf/issues)

We will get back to you as soon as possible.
