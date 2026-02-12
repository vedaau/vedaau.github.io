---
title: Power Budget
tags:
- tag1
- tag2
---

## Overview
The power budget analysis ensures that all subsystem components operate within the voltage regulator's capabilities and that sufficient current is available for typical and maximum operating conditions. The analysis includes power consumption calculations and safety margins to guarantee reliable operation.

## Power Budget

*Table 1: Subsystem Power Budget*

| **Component** | **Voltage (V)** | **Typical Current (mA)** | **Max Current (mA)** | **Typical Power (mW)** | **Max Power (mW)** |
|---------------|-----------------|--------------------------|----------------------|------------------------|---------------------|
| Microcontroller | 3.3 | 20 | 40 | 66 | 132 |
| Voltage Regulator | 3.3 | 5 | 10 | 16.5 | 33 |
| Microphone | 3.3 | 1 | 2 | 3.3 | 6.6 |
| **Total** | - | **26** | **52** | **85.8** | **171.6** |

## Analysis

With a total typical power consumption of 85.8 mW and maximum of 171.6 mW, the subsystem operates well within the TC1264-3.3VAB voltage regulator's 500mA capacity, providing ample safety margin for reliable operation.
