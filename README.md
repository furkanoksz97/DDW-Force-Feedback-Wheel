\# DIY Direct Drive Force Feedback Wheel



A DIY Direct Drive Force Feedback steering wheel developed using a hoverboard BLDC motor and ODrive S Mini.



The project was developed step by step by combining commercially available components with custom hardware, firmware and mechanical design.



The goal of this repository is to document the complete development process so that others who want to build a similar system can follow the same path, understand the connections and use the project as a starting point for their own Direct Drive wheel.



\---



\## Features



\* Direct Drive Force Feedback

\* Hoverboard BLDC motor

\* ODrive S Mini motor controller

\* 1000 PPR rotary encoder

\* FFBeast Force Feedback system

\* Logitech G27 pedals

\* Logitech G27 shifter

\* Arduino Pro Micro shifter controller

\* Custom steering wheel housing

\* UART interface for future expansion



\---



\## Hardware



\### Main System



\* Hoverboard BLDC motor

\* ODrive S Mini

\* 24 V / 20 A power supply

\* 2.2 Ω / 100 W aluminum braking resistor

\* 1000 PPR incremental rotary encoder

\* 10 kΩ pull-up resistors for encoder A/B signals



\### Pedals



\* Logitech G27 pedal set

\* Connected directly to ODrive S Mini GPIO inputs

\* Powered from the ODrive S Mini 5 V output



\### Shifter



\* Logitech G27 shifter

\* Arduino Pro Micro

\* Custom firmware

\* UART interface for future expansion



\---



\## Software



\* FFBeast

\* Arduino / Pro Micro firmware

\* Custom shifter firmware



For detailed information about FFBeast:



\[FFBeast Official Website](https://ffbeast.github.io/)



\---



\## Development Process



The system was developed incrementally, testing each major part before moving to the next stage.



\### 1. BLDC Motor



The project started with a hoverboard BLDC motor.



The motor was selected as the main actuator for the Direct Drive system.



\### 2. ODrive S Mini



An ODrive S Mini was added to control the BLDC motor.



The motor phases were connected according to the motor winding sequence.



A 24 V / 20 A metal-case power supply was used to power the system.



\### 3. Brake Resistor



The braking resistor was replaced with a 2.2 Ω / 100 W aluminum resistor.



The resistor was used to dissipate regenerative energy generated during rapid motor deceleration and Force Feedback reactions.



\### 4. Rotary Encoder



A 1000 PPR incremental rotary encoder was integrated for steering position feedback.



10 kΩ pull-up resistors were used on the A and B signal lines to provide stable digital signal levels.



\### 5. Force Feedback



FFBeast was integrated with the motor controller and encoder to provide Force Feedback functionality.



The system was tested before moving on to the additional peripherals.



\### 6. Logitech G27 Pedals



The original Logitech G27 pedals were integrated into the ODrive S Mini.



The pedal signals were connected to the ODrive S Mini GPIO inputs and the pedals were powered using the board's 5 V output.



\### 7. Custom Steering Housing



A custom steering housing was designed around the actual components used in the project.



The housing was manufactured and assembled with the Direct Drive system.



\### 8. Logitech G27 Shifter



The original Logitech G27 shifter was integrated using an Arduino Pro Micro.



The Pro Micro reads the shifter's digital button signals and X/Y axis positions, determines the selected gear and communicates the shifter state to the PC.



\### 9. Testing



The completed system was tested in racing games.



The steering, Force Feedback, pedals and shifter operated correctly as a complete sim racing system.



\---



\## Project Status



\*\*Working\*\*



The current version of the system has been successfully assembled and tested in racing games.



The main Direct Drive system, pedals and G27 shifter are functional.



The UART interface is available for future system expansion.



\---



\## Documentation



Detailed information about each development stage can be found in the corresponding folders:



\* \[BLDC Motor](01-BLDC-Motor/)

\* \[ODrive S Mini](02-ODrive-S-Mini/)

\* \[Rotary Encoder](03-Encoder/)

\* \[FFBeast](04-FFBeast/)

\* \[G27 Pedals](05-G27-Pedals/)

\* \[Steering Housing](06-Steering-Housing/)

\* \[G27 Shifter](07-G27-Shifter/)

\* \[Testing](08-Testing/)



\---



\## Future Development



The project can be further expanded with additional controllers, communication interfaces and hardware improvements.



The UART interface between the custom controller and the motor control system provides a foundation for future development.



Additional documentation, wiring diagrams, photographs and CAD files will be added as the project is updated.



