# custom end-to-end mechanical keyboard + joystick 
this repository documents the end-to-end hardware engineering of a specialized mechanical input device. unlike traditional boards, this project focuses on **low-latency analog integration** and a layout specifically tuned for the **frantic multitasking required in Overcooked2**. standard keyboards rely on binary WASD inputs, which can feel clunky during a level 6-4 rush. by integrating a dedicated **analog joystick** directly into the PCB layout, this project allows for 360-degree fluid movement while maintaining the tactile precision of **mechanical switches** for chopping, dashing, and throwing.

##
i'm currently in the **schematic capture** and **PCB design** phase, exploring custom electrical architecture.

the following are key areas of development: 
* **joystick integration**: developing the circuitry to interface an analog thumbstick (via ADC pins) alongside a traditional switch matrix
* **circuit analysis**: conducting research into matrix scanning logic and signal integrity to ensure zero-latency response times during peak gameplay
* **PCB layout**: routing the traces for a custom form factor, prioritizing ergonomic joystick placement to reduce thumb strain

my roadmap includes and is not limited to: 
  * **custom firmware**: writing specialized QMK/ZMK logic to map the joystick as an X-input controller or high-speed directional keys
  * **fabrication**: sending the first revision of the PCB for manufacturing and hand-soldering the SMD components
  * **enclosure design**: CAD modelling a low-profile case that supports the extra vertical height of the joystick assembly
  * **custom configuration GUI**: allowing real-time customization without requiring the user to recompile C code or flash firmware manually

the technical stack: 
  * **EDA**: KiCad 9.0
  * **CAD**: OnShape 
  * **microcontroller**: RP2040
  * **input hardware**: mechanical switches + 2-axis analog potentiometer
  * **firmware**: QMK with custom Analog-to-HID mapping logic
  * **target performance**: 1000Hz polling rate for frame-perfect dashing 
