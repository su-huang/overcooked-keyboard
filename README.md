# custom end-to-end mechanical keyboard + joystick 
this repository documents the end-to-end hardware engineering of a specialized mechanical input device. unlike traditional boards, this project focuses on low-latency analog integration and a layout specifically tuned for the frantic multitasking required in overcooked2. standard keyboards rely on binary wasd inputs, which can feel clunky during a level 6-4 rush. by integrating a dedicated analog joystick directly into the pcb layout, this project allows for 360-degree fluid movement while maintaining the tactile precision of mechanical switches for chopping, dashing, and throwing.

##
i'm currently in the schematic capture and pcb design phase, exploring custom electrical architecture.

the following are key areas of development: 
* joystick integration: developing the circuitry to interface an analog thumbstick (via adc pins) alongside a traditional switch matrix
* circuit analysis: conducting research into matrix scanning logic and signal integrity to ensure zero-latency response times during peak gameplay
* pcb layout: routing the traces for a custom form factor, prioritizing ergonomic joystick placement to reduce thumb strain

my roadmap includes and is not limited to: 
  * custom firmware: writing specialized qmk/zmk logic to map the joystick as an x-input controller or high-speed directional keys
  * fabrication: sending the first revision of the pcb for manufacturing and hand-soldering the smd components
  * enclosure design: cad modelling a low-profile case that supports the extra vertical height of the joystick assembly
  * custom configuration gui: allowing real-time customization without requiring the user to recompile c code or flash firmware manually

the technical stack: 
  * eda: kicad 
  * cad: onshape 
  * microcontroller: rp2040
  * input hardware: mechanical switches + 2-axis analog potentiometer
  * firmware: qmk with custom analog-to-hid mapping logic
  * target performance: 1000hz polling rate for frame-perfect dashing 
