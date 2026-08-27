# \# Logitech G27 Shifter

# 

# The original \*\*Logitech G27 shifter\*\* was integrated into the custom Direct Drive system using an \*\*Arduino Pro Micro\*\*.

# 

# The Pro Micro reads the G27 shifter's button and X/Y axis signals, determines the selected gear and communicates the shifter state to the PC.

# 

# \## G27 Shifter → Pro Micro

# 

# The shifter was connected to the Pro Micro as follows:

# 

# | G27 DB9 | Function                | Pro Micro     |

# | ------: | ----------------------- | ------------- |

# |       1 | Button Clock            | D0            |

# |       2 | Button Data             | D1            |

# |       3 | Button !CS / !PL (Mode) | D4            |

# |       4 | Shifter X Axis          | D8 / A8       |

# |       5 | SPI Input               | Not connected |

# |       6 | GND                     | GND           |

# |       7 | +5 V                    | VCC           |

# |       8 | Shifter Y Axis          | D9 / A9       |

# |       9 | +5 V                    | VCC           |

# 

# These connections allow the Pro Micro to read both the digital button states and the analog X/Y position of the G27 shifter.

# 

# \## Gear Detection

# 

# The X and Y axis values are read by the Pro Micro and compared against predefined thresholds to determine the selected gear.

# 

# The system supports:

# 

# \* Neutral

# \* 1st gear

# \* 2nd gear

# \* 3rd gear

# \* 4th gear

# \* 5th gear

# \* 6th gear

# \* Reverse

# 

# Reverse is detected using the reverse button when the shifter is positioned in the 6th-gear position.

# 

# \## UART Communication

# 

# The Pro Micro also uses its `Serial1` UART interface at \*\*115200 baud\*\*.

# 

# When the selected gear changes, the controller sends the corresponding gear information through UART:

# 

# ```text

# GEAR:N

# GEAR:R

# GEAR:1

# GEAR:2

# GEAR:3

# GEAR:4

# GEAR:5

# GEAR:6

# ```

# 

# The message is transmitted only when the gear changes.

# 

# This UART interface was used as a communication path for future system expansion and external controller integration.

# 

# > The Pro Micro UART output is documented here. The external controller's UART pin assignments are not specified in this firmware and should be documented separately.

# 

# \## Custom Firmware

# 

# The Pro Micro firmware handles:

# 

# \* G27 shifter button reading

# \* X/Y axis reading

# \* Gear detection

# \* Reverse detection

# \* USB HID communication

# \* UART gear communication

# 

# The firmware continuously reads the shifter position and button states, determines the current gear and sends the resulting state to the PC through the G27 HID interface.

# 

# \## Testing

# 

# The completed G27 shifter was integrated into the Direct Drive system and tested in racing games.

# 

# The shifter operated correctly together with the steering wheel and pedals.



