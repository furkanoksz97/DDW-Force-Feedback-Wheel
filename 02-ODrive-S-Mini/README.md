\# ODrive S Mini



After selecting the hoverboard BLDC motor, an \*\*ODrive S Mini\*\* was used as the motor controller for the Direct Drive Force Feedback system.



\## Motor Connection



The three motor phase wires were connected to the ODrive according to the motor winding sequence.



The motor was powered from a \*\*24 V / 20 A metal-case switching power supply\*\*.



\## Brake Resistor



The original braking resistor was replaced with a \*\*2.2 Ω / 100 W aluminum resistor\*\*.



The reason for this modification was to handle the regenerative energy generated during rapid changes in motor speed and aggressive Force Feedback reactions.



When the motor is rapidly decelerated or driven by an external force, it can operate temporarily as a generator and return energy to the DC bus. The brake resistor dissipates this energy as heat and helps prevent excessive DC bus voltage rise.



The aluminum resistor was selected to provide better thermal behavior during repeated braking events.



\## Rotary Encoder



A \*\*1000 PPR incremental rotary encoder\*\* was used for steering position feedback.



The encoder provides \*\*A and B quadrature signals\*\*, allowing the controller to determine both steering position and direction of rotation.



\*\*10 kΩ pull-up resistors\*\* were added to the A and B signal lines.



The pull-up resistors were used to keep the digital signal levels stable and provide a defined HIGH level when the encoder output is not actively pulling the signal LOW. This improves signal reliability and reduces the possibility of floating or unstable logic levels.



> Note: The pull-up resistors are used for signal conditioning and reliable logic-level detection; they are not primarily intended as protection for the encoder.



\## Result



After integrating the BLDC motor, ODrive S Mini, brake resistor and rotary encoder, the motor control system was ready for the Force Feedback stage.



