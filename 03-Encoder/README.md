\# Rotary Encoder



A \*\*1000 PPR incremental rotary encoder\*\* was used to measure the steering wheel position.



The encoder provides two digital signals, \*\*A and B\*\*, which form a quadrature signal. By monitoring the phase relationship between these two signals, the direction and relative position of the steering wheel can be determined.



\## Signal Connection



The encoder's A and B output signals were connected to the controller inputs.



A \*\*10 kΩ pull-up resistor\*\* was added to both the A and B signal lines.



The pull-up resistors provide a defined HIGH logic level when the encoder output is not actively pulling the signal LOW. This helps prevent floating inputs and improves the reliability of the encoder signals, especially at higher signal frequencies.



\## Purpose



The encoder provides the steering position feedback required by the Force Feedback control system.



The encoder was tested together with the ODrive S Mini and the system operated correctly.



\## Specifications



| Parameter           | Value                      |

| ------------------- | -------------------------- |

| Type                | Incremental Rotary Encoder |

| Resolution          | 1000 PPR                   |

| Signals             | A / B                      |

| Signal conditioning | 10 kΩ pull-up              |

| Application         | Steering position feedback |



