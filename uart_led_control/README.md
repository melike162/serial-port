# UART LED Control Project

This project demonstrates **LED control** using the **STM32F407VGT6** microcontroller and a **C# Windows Forms** interface over UART communication.  

## Project Contents

1. **STM32 CubeIDE Code (`led_cubeide`)**
   - Receives data via UART4 using interrupt mode.
   - Controls LEDs on PD12-PD15 based on received commands.
   - Sends an acknowledgment back for each received command. Example: Receiving '1' turns on LED1 and sends back '2'.

2. **C# Windows Forms Interface (`led_c`)**
   - Allows selection of COM port and baud rate from PC.
   - Sends LED control commands to STM32 ('1', '3', '5', '7') via button clicks.
   - Displays incoming UART data in a TextBox.
   - Manages connection status (Connect/Disconnect).

## Requirements

- **STM32 CubeIDE** and STM32F407G DISC1 (or equivalent board)
- **Visual Studio 2022** or newer for the C# Windows Forms application
- USB-UART cable or built-in virtual COM port on STM32

## Usage

1. **STM32**
   - Compile and upload the project using CubeIDE.
   - Connect the STM32 board to your computer.

2. **C# Interface**
   - Open and compile the program in Visual Studio.
   - Select the COM port and baud rate, then click Connect.
   - Use the LED buttons to control LEDs on the STM32 board.
   - Incoming data will be displayed in the TextBox.
