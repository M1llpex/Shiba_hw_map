# Google "Shiba" (Zuma SoC) Hardware Map

This repository contains a detailed, community-driven hardware map for the Google device codenamed **"Shiba,"** which is based on the **"Zuma"** System-on-Chip (SoC). The information is presented in the form of Device Tree Source Include (`.dtsi`) files, meticulously organized by hardware component.

## DISCLAIMER

***This hardware map is the result of reverse engineering and data analysis. It is not an official release from Google. While extensive effort has been made to ensure accuracy, the information is provided "as-is" without any guarantees. Use this information at your own risk.***

-----

## Hardware Overview

The Shiba device features a complex and powerful set of hardware components, all orchestrated by the Zuma SoC.

### 🧠 Core System-on-Chip (SoC)

  * **SoC:** Google Zuma
  * **CPU:** 9-core, 64-bit ARMv9 CPU in a tri-cluster configuration:
      * **LITTLE Cluster (Efficiency):** 4x "Klein" cores (Cortex-A510 equivalent) up to 1.70 GHz
      * **MID Cluster (Performance):** 4x "Makalu" cores (Cortex-A710 equivalent) up to 2.37 GHz
      * **BIG Cluster (Prime):** 1x "Makaluelp" core (Cortex-X2 equivalent) up to 2.91 GHz
  * **GPU:** ARM Mali-G715 with detailed DVFS (Dynamic Voltage and Frequency Scaling) and thermal configurations.
  * **NPU (Neural Processing Unit):**
      * Google EdgeTPU ("Rio") for machine learning acceleration.
      * Google GXP DSP ("Callisto") for low-power signal processing.
  * **Memory:** LPDDR5 RAM.
  * **Interrupt Controller:** ARM Generic Interrupt Controller v3 (GICv3).

-----

### 📸 Camera & Imaging

The Shiba device includes a sophisticated multi-camera system with a variety of sensors, actuators, and supporting components.

  * **Rear Camera System:**
      * **Main Sensor:** "Boitata"
      * **Ultrawide Sensor:** "Sandworm"
      * **Actuators & OIS:** "Cornerfolk" and "Djinn" components for focus and stabilization.
  * **Front Camera System:**
      * **Sensor:** "Dokkaebi"
  * **Supporting Hardware:**
      * Laser Detect Autofocus (LDAF) / Time-of-Flight (ToF) sensor.
      * Multiple EEPROM modules ("Djinn," "Smaug") for storing calibration data.
      * Dedicated power supplies and I2C buses for each camera component.

-----

### 🔋 Power & Charging

  * **Charging ICs:** A multi-chip solution including NXP PCA9468, Renesas P9221, and Maxim MAX77759 to manage both wired and wireless charging.
  * **Wireless Charging:** Support for the Qi standard, including EPP and HPP protocols with detailed Foreign Object Detection (FOD) parameters.
  * **Battery Management:** Google Battery Management System (GBMS) and a Maxim Fuel Gauge (maxfg) for accurate battery monitoring.
  * **PMICs (Power Management ICs):** Dual S2MPG14 and S2MPG15 PMICs managing a wide array of power rails for every subsystem, from the CPU cores to the smallest sensors.

-----

### 🖥️ Display & Touch

  * **Display Panels:** Support for two distinct DSI-based panels, codenamed "Bigsurf" and "Shoreline."
  * **Touch Controller:** A Goodix `brl-d` series SPI-based touch controller, with support for features like an under-display fingerprint sensor (UDFPS).

-----
    // ... additional board-level definitions ...
};
```
