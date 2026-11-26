# REV 1.1 – Scalable 9-Input Matrix & Code Refactoring

Architectural upgrade expanding the prototype from 2 hardcoded inputs to a full **9-button control array** (`BTN_1` through `BTN_9`), testing the target layout of the handheld remote.

## Key Features
* **9-Channel GPIO Input:** Configured `PA0-WKUP`, `PA1`, `PA4`, `PB0`, `PB1`, and `PC0..PC3` with internal pull-ups, while keeping `I2C1` and `SPI1` pins reserved for future OLED and RF modules.
* **Struct-Based Polling Loop:** Refactored repetitive `if` blocks into a scalable `for` loop iterating over an array of button structures (port, pin, command string), keeping `main.c` clean and maintainable.
* **Full Host Command Mapping:** Added support for playback controls (`Next`, `Pause`, `Prev`, `Shuffle`, `Wake-up`, `Loop`), volume presets (`1%`, `5%`, `15%`).

## Prototype Setup
![9-Button Prototype Wiring](../../progression/rev1_1_wiring.jpg)
