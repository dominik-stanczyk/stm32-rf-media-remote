# REV 1.0 – UART Communication & Host Media Control

First functional prototype integrating the STM32 microcontroller with the PC-side Python server (**home-media-controller**). This revision introduces serial communication over `USART2` and imperfect debouncing to control live media playback (YouTube).

## Key Features
* **Serial Interface (`USART2`):** Configured at `115200 bps` (8N1) via the on-board ST-LINK Virtual COM Port (`PA2`/`PA3`).
* **Dual-Button Input (`PA0`, `PA1`):** Mapped physical triggers to `pause` and `next` ASCII commands terminated with `\n`.
* **Software Debouncing:** Implemented a `30 ms` stabilization delay and release-wait loop to eliminate mechanical contact bounce and prevent command flooding.
* **End-to-End Integration:** Verified real-time command execution from physical hardware trigger -> UART -> Python `pyserial` -> WebSocket -> Browser Extension.

## Hardware & Demo
![Two-Pin UART Prototype](../../progression/rev1_0_setup.jpg)

<!-- >> **Video Demo:** *LINK GDY FILM BĘDZIE GOTOWY* -->
