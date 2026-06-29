# MCC Harmony for SAMD21 - Send ASCII via UART + DMA

Send **ASCII art** stored in flash memory to a terminal  
using **UART communication with DMA transfer** on ATSAMD21J18A, configured via MCC Harmony.

## 📹 Video Tutorial
https://youtu.be/DglVz1QhKXs

## 🛠️ Tools & Hardware

- MPLAB X IDE
- MCC Harmony
- SAMD21 Xplained Pro (ATSAMD21-XPRO)
- Terminal emulator (e.g. Tera Term, PuTTY)

## 📋 What it does

- Stores Garfield ASCII art as a "const uint8_t[]" array in flash (garfield.c)
- Uses **DMAC Channel 0** to transfer the entire array to **SERCOM3 UART** — no CPU involvement during transfer
- Garfield appears in the terminal upon reset 🐱
