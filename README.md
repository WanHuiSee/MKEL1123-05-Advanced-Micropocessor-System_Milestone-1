# MKEL1123-05 Advanced Microprocessor System
# Youtube Link : [GROUP 3 : STM FAMILIARIZATION (MILESTONE 1)](https://youtu.be/YOWYuShPGjM)
# Milestone 1: STM Familiarization
## Overview
**Group 3**
<br>  Group Member: 
| **Name** | **Matrics Number** |
| :-----------: | :-----------: |
| Kukenraj a\l K.Pugalenthy | MKE211088 |
| Low Q' Ying | MKE211099 |
| See Wan Hui | MKE211093 |

## 1.0 Objectives
- To familiarize with basic STM32 firmware development.
- To verify the operation of STM32 board.
- To familiarize with Github for reporting milestones.

## 2.0 Equipments and Softwares
### 2.1 Equipments Required
- Microcontroller board with Cortex-M4 based processor, STM32F446 Nucleo-64 (STM32F446RET6 64 PINS)
- Personal computer 
- USB Type-A to Mini-B cable

#### 2.1.1 Features of STM32F446 Nucleo-64 Microcontroller Board
- ARM Cortex-M4 180 MHz
- 512-KB Flash, 128-KB SRAM
- Includes two extension connectors:
  - Arduino Uno
  - ST morpho
- Embedded ST-LINK/V2-1 debugger with USB re-enumeration capability such as:
  - mass storage
  - virtual communication (COM) port
  - debug port
- mbed-enabled
- Support multiple Integrated Development Environments (IDEs):
  - IAR Embedded Workbench
  - MDK-ARM
  - STM32CubeIDE

#### 2.1.2 Photo of STM32F446 Nucleo-64 Microcontroller Board
![STM32F446](https://user-images.githubusercontent.com/104665552/166263426-0b241e42-8453-40ed-a001-4d175e213135.jpeg)


### 2.2 Softwares
#### 2.2.1 STM32CubeIDE
- All-in-one multi-OS development tool for Windows, Linux, and macOS with 64-bit versions only.
- Provide an advanced platform for C/C++ development with peripheral configuration
- Code generation and code compilation
- Advanced debug features for STM32 microcontrollers and microprocessors 
- Support for ST-LINK (STMicroelectronics) and J-Link (SEGGER) debug probes

#### 2.2.2 USB Driver (STSW-LINK009)
- A digitally signed driver which allow successful USB interfaces between the device

## 3.0 Methodology
### 3.1 Procedure
1. The microcontroller board was connected with a personal computer via USB Type-A to Mini-B cable.
2. The STM32CubeIDE and USB Driver (STSW-LINK009) softwares were downloaded and installed.
3. The STM32CubeIDE software was run.
4. New project was created.
5. The GPIO Output Pin was configured within the STM32CubeIDE Configuration Tool.
6. The HAL_GPIO_Write was used to change the pin state and the HAL_Delay() was used to create time delay for operation.
7. Unique coding was applied in the STM32CubeIDE software to create a blinky(can be found in main.c).
8. The application project was then built.
9. The code could then be downloaded and programmed into the microcontroller board.

### 3.2 Source Code (In detail)
- This code is to test the connection between switch and led blinking for 1Hz
 ```
  while (1)
  {
    if(!HAL_GPIO_ReadPin(GPIOC,GPIO_PIN_13))
    {
    	HAL_GPIO_TogglePin(LD2_GPIO_Port, LD2_Pin);
    	HAL_Delay(1000);
    }
    else
    {
    	HAL_GPIO_WritePin(LD2_GPIO_Port, LD2_Pin, GPIO_PIN_RESET);
    }
  }
  ```
- For full code, please refer to the main.c file.

## 4.0 References 
### 4.1 Tutorial Videos
1. [50. Install STM32CubeIDE and LED blink program with Nucleo for Windows](https://www.youtube.com/watch?v=oAwZ0cjlmN8)
2. [Getting Started with STM32 and Nucleo Part 1: Introduction to STM32CubeIDE and Blinky – Digi-Key](https://www.youtube.com/watch?v=hyZS2p1tW-g)

### 4.2 Websites
1. “NUCLEO-F446RE - STM32 Nucleo-64 development board with STM32F446RE MCU, supports Arduino and ST morpho connectivity - STMicroelectronics,” www.st.com. https://www.st.com/en/evaluation-tools/nucleo-f446re.html.
2. “STM32CubeIDE - Integrated Development Environment for STM32 - STMicroelectronics,” www.st.com. https://www.st.com/en/development-tools/stm32cubeide.html#:~:text=STM32CubeIDE%20is%20an%20all%2Din.
3. “STSW-LINK009 - ST-LINK, ST-LINK/V2, ST-LINK/V2-1, STLINK-V3 USB driver signed for Windows7, Windows8, Windows10 - STMicroelectronics,” www.st.com. https://www.st.com/en/development-tools/stsw-link009.html
