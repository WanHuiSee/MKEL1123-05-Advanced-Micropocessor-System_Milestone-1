# Milestone-1
Group 3
Group Member: 
| Syntax | Description |
| ----------- | ----------- |
| **Name** | **Matrics Number** |
| Kuken |  |
| Low Q'Ying | MKE |
| See Wan Hui | MKE211093 |

## 1.0 Equipment
- Microcontroller board with Cortex-M4 based processor, STM32F446 Nucleo-64 (STM32F446RET6 64 PINS)
- Personal computer 
- USB Type-A to Mini-B cable

### 1.1 Features of STM32F446 Nucleo-64 Microcontroller Board
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

### 1.2 Photo of STM32F446 Nucleo-64 Microcontroller Board
![alt text](STM32F446.jpeg)
![STM32F446](https://user-images.githubusercontent.com/104665552/166263426-0b241e42-8453-40ed-a001-4d175e213135.jpeg)


## 2.0 Software
### 2.1 STM32CubeIDE
- All-in-one multi-OS development tool for Windows, Linux, and macOS with 64-bit versions only.
- Provide an advanced platform for C/C++ development with peripheral configuration
- Code generation and code compilation
- Advanced debug features for STM32 microcontrollers and microprocessors 
- Support for ST-LINK (STMicroelectronics) and J-Link (SEGGER) debug probes

### 2.2 USB Driver (STSW-LINK009)
- A digitally signed driver which allow successful USB interfaces between the device

## 3.0 Procedure
1. Connect the microprocessor with a personal computer via USB Type-A to Mini-B cable.

### Source Code
 `while (1)
  {
	  HAL_GPIO_WritePin(GPIOA, GPIO_PIN_5, 1);
	  HAL_Delay(1000);
	  HAL_GPIO_WritePin(GPIOA, GPIO_PIN_5, 0);
	  HAL_Delay(1000);
    /* USER CODE END WHILE */

    /* USER CODE BEGIN 3 */
  }`
  
## 4.0 Referenced Tutorials 
### 4.1 Tutorial Video:
[50. Install STM32CubeIDE and LED blink program with Nucleo for Windows](https://www.youtube.com/watch?v=oAwZ0cjlmN8)

## 5.0 References
https://www.st.com/en/evaluation-tools/nucleo-f446re.html
https://www.st.com/en/development-tools/stm32cubeide.html#:~:text=STM32CubeIDE%20is%20an%20all%2Din,for%20STM32%20microcontrollers%20and%20microprocessors.
https://www.st.com/en/development-tools/stsw-link009.html
