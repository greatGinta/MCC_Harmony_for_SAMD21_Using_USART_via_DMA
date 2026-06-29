MCC Harmony for SAMD21 - Send ASCII Art via UART + DMA

Send Garfield ASCII art stored in flash memory to a terminal

using UART communication with DMA transfer on SAMD21, configured via MCC Harmony.

🛠️ Tools & Hardware


MPLAB X IDE
MCC Harmony
SAMD21 Xplained Pro
Terminal emulator (e.g. Tera Term, PuTTY)


📋 What it does


Stores a Garfield ASCII art image as a const uint8_t[] array in flash (garfield.c)
Uses DMAC Channel 0 to transfer the entire array to SERCOM3 UART in one shot — no CPU involvement during transfer
Initializes all peripherals via SYS_Initialize() then triggers the DMA transfer immediately on boot
