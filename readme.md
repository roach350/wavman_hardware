# WAVMAN Hardware
## WAVMAN Overview
WAVMAN is an open source portable PCM audio player based around the ATSAMD21 serieis of microcontrollers and the PCM5102 DAC. It supports SD via an SPI interface.

## Revisions and Notes
### REV 0
- Wrong symbol for USB-C resulting in only one pair of DP/DM being connected
- DAC does not have 3.3v on VDDIO or VDDIN
- PCM_MUTE (DAC mute) is not connected to MCU or even a pull up resistor to 3.3v so DAC is always muted by default
- The hold switch was botched (not connected to MCU and wrong net for power)
- All displays sink current from the LDO instaed of the battery directly, it may be desirable to change this
- No dedicated debug port for SWCLK and SWDIO
- The audio amp. has is missing several compontents (feedback resistors Rf and decoupling cap.)
- AMP_SHUTDOWN is not connected to the MCU
### REV 1
- should fix all major issues with REV 0
- minor tweaks to switch and knob placement
- 0805 passive components
- rerouted audio ICs
- knockout silkscreen for userfacing text 
