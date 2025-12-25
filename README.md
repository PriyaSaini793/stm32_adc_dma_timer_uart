# Timer Triggered ADC using DMA and UART on STM32F411

## Overview
This project demonstrates timer-triggered ADC conversion using DMA and UART communication on STM32F411 microcontroller.

## Features
- Timer 2 configured at 100 Hz
- ADC triggered by TIM2 TRGO
- ADC data transferred using DMA in circular mode
- UART2 used to transmit ADC values to PC
- STM32 HAL drivers used

## Peripherals Used
- ADC1 (Channel 0)
- TIM2 (Trigger Output)
- DMA2 Stream 0
- USART2 (115200 baud)

## Working
1. TIM2 generates a trigger event at 100 Hz
2. ADC conversion starts on each trigger
3. DMA transfers ADC result to memory
4. DMA completion callback sends ADC value over UART

## Tools Used
- STM32CubeMX
- STM32CubeIDE
- STM32 HAL Library

## Output
ADC values are transmitted over UART every 10 ms.

## Note
Project compiled and verified successfully. Hardware execution requires STM32F411 board.
