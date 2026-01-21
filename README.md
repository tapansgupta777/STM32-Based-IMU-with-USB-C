## STM32-Based Inertial Measurement Unit (IMU) Module with USB-C

### 1. Project Overview

This project presents a **custom STM32-based IMU development module** built around the **STM32F411CEU6** microcontroller and the **MPU-6050** six-axis inertial sensor. The board is engineered as a compact and efficient motion-sensing platform intended for embedded experimentation, control systems, and sensor-fusion applications.

A **USB Type-C interface** is employed as the primary power and data connection, offering improved connector reliability, reversible plug orientation, and enhanced mechanical robustness compared to legacy USB solutions. The overall hardware architecture is influenced by modern STM32 reference designs, with careful adaptation and validation of design choices to suit the IMU-centric application.

The complete schematic capture and PCB layout were carried out in **Altium Designer**, adhering to industry-accepted practices for power integrity, grounding strategy, and high-speed signal routing.

---

### 2. Key Specifications

**Microcontroller**
- STM32F411CEU6 (ARM Cortex-M4 with floating-point unit support)

**Inertial Sensor**
- MPU-6050 6-axis IMU (3-axis accelerometer + 3-axis gyroscope)
- Communication via I²C bus

**Power Architecture**
- Input supply: 5V provided through **USB Type-C connector**
- On-board LDO converts 5V to a regulated 3.3V rail for MCU and sensor operation

**Communication & Debugging**
- I²C interface for real-time motion data acquisition
- SWD (Serial Wire Debug) interface for firmware programming and debugging

**PCB Implementation**
- 4-layer printed circuit board:
  - Layer 1: Signal routing  
  - Layer 2: Continuous ground plane  
  - Layer 3: Dedicated ground plane for noise reduction  
  - Layer 4: Signal routing  

This multilayer stack-up enhances signal integrity, minimizes EMI, and ensures stable operation of both the microcontroller and inertial sensor.

---

### 3. Design Highlights

- USB-C interface improves durability and usability  
- Clean power distribution with dedicated ground planes  
- Compact layout optimized for embedded and motion-tracking use cases  
- Design choices documented and verified through schematic-to-layout consistency checks
