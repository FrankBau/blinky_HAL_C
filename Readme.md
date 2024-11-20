A blinky in C for the STM Nucleo-L432KC board using STM32CubeMX and HAL.

STM32CubeMX features a GUI for MCU configuration, pin planning, clock settings and so on.
This is a great tool for getting started and more complex projects.
The wording in the menues does always not correspond to the reference manual or other useful documentation which can cause trouble.

Using the Hardware Abstraction Layer (HAL) libraries makes the code more portable and, maybe, more readable.

The additional HAL layer clearly introduces overhead and possibly bugs and should not be used wthout a critical review.

HAL is well suited for getting acquainted to peripheral compontents like SPI, I2C, timers. 
HAL is open source, you can step into the code and learn how it works.

Using HAL may be advantageous when using heavy software libraries like for USB, Ethernet, RTOS,...

In principle, HAL generated code can be switchted to low-level (LL) code later on a component basis
and easily combined with register level code where needed (interrupt handlers, advanced DMA-IRQ usage,..) 

STM32CubeMX copied the complete HAL and LL code into the project. This is overkill for a blinky and could have been configured otherwise. It is just here for demo.

Recommended workflow.