---
title: Microcontroller Code
---

## Overview

This section contains the microcontroller code for the AutoCan project. This code controls a bidirectional motor based on a digital input signal. If the input is HIGH, it turns on an LED and drives the motor forward; if the input is LOW, it turns the LED off and drives the motor in reverse. The program continuously monitors the input and updates the motor direction in an infinite loop.

## Code 

```
/*Vedaa Ubale
 EGR 304- TEAM 202 (Lid motor subsystem)*/

#include "mcc_generated_files/system/system.h"

void motor_stop(void)
{
    REV_SetLow();
    FWD_SetLow();
}

void motor_forward(void)
{
    REV_SetLow();
    FWD_SetHigh();
    __delay_ms(10);
}

void motor_reverse(void)
{
    FWD_SetLow();
    REV_SetHigh();
    __delay_ms(10);
}

int main(void)
{
    SYSTEM_Initialize();
    
    motor_stop();
    DEBUG_LED_SetLow();
    
    while(1)
    {
       //DEBUG_LED_SetHigh();
        if (DIGIN_GetValue() == 1)
        {
            DEBUG_LED_SetHigh();
            
            motor_forward();   
        }
        else
        {
            DEBUG_LED_SetLow();
            motor_reverse();
        }
    }
    return 0;
}
 
```


## Resources

This is the project code zip file:[Microcontroller code](motor_subsystem.zip) 



