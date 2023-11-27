# Arm_STM32
Space for rover robotic arm motion_controller

# Things needed to be done

## MXCube
- [ ] Create STM32F446 project
- [ ] Initialize the periphery:
    - [ ] (6x) Timers for steppers
    - [ ] (6x) Dirs
    - [ ] (6x) Stallguards?
    - [ ] (6x) Encoders?
    - [ ] (2x) TMC Drivers UART
    - [ ] (1x) UART for communication with main system (115200 baudrate)

## Communication
- [ ] Make a small reseatch (DF1 structure?)
- If research sucks:
    - [ ] Reading UART buffer over DMA
    - [ ] Create data format: [cmd][data][crc][nullch] Byte stuffing before or after -> GPT
    - [ ] Implement CRC
    - [ ] implement byte-stuffing
    - [ ] Check the matlab side
- else:
    - [ ] Implement found solution

## Stepper motor control

- [ ] Think about the buffering and the timing
- [ ] Create C stepper with ISR switch case ACC/LIN/DEC
- [ ] Create Buffer for ISR phases
- [ ] Create precalculation in main loop
- [ ] Measure length of execution
- [ ] Check the accuracy of movements

## Bonus things:
- [ ] Learning mode?
- [ ] PID mode?
- [ ] ???