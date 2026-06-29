MCC Harmony for SAMD21 - Using USART via DMA
Demonstrate how to transfer a large image array (ASCII Art)
directly from memory to serial port using DMA communication on SAMD21, configured via MCC Harmony.

📹 Video Tutorial
https://www.youtube.com/watch?v=@GreatGinta

🛠️ Tools & Hardware
MPLAB X IDE

MPLAB Harmony v3 / MCC

ATSAMD21G18A

Serial Terminal (TeraTerm / Putty)

📋 What it does
Zero CPU Overhead: The CPU triggers the DMA controller just once inside the main() function.

Background Streaming: Hardware DMA Channel 0 takes full responsibility for streaming a massive byte array out through the SERCOM3 USART peripheral.

Non-blocking Runtime: The main CPU remains 100% free inside the execution loop (while(true)) to process background system tasks (SYS_Tasks) without any lagging or stuttering.
