# REV 0.0 – Hardware Bring-up & GPIO Input Test

Initial hardware validation on the **STM32F446RE Nucleo** board. The goal of this revision was to verify the toolchain setup (STM32CubeMX + STM32CubeIDE), test basic GPIO output control, and validate internal pull-up resistors using a physical jumper wire trigger.

## Key Features
* **Toolchain Bring-up:** Configured clock tree and basic peripherals using STM32CubeMX.
* **GPIO Output (`PA5`):** On-board user LED (`LD2`) control.
* **GPIO Input (`PA0-WKUP`):** Configured with an internal pull-up resistor (`~40 kΩ`). Shorting `PA0` to `GND` pulls the line low (`GPIO_PIN_RESET`) and triggers the LED.
* **Live Register Debugging:** Verified real-time bit manipulation directly in the `GPIOA->ODR` Special Function Register via ST-LINK debugger.

## Hardware & Demo
![Nucleo F446RE Setup](../../progression/rev0_setup.jpg)

<!-- >> **Video Demo:** *(LINK gdy będzie gotowy na YT)* -->
