# WAVMAN Hardware
## WAVMAN Overview
WAVMAN is an open source portable PCM audio player based around the ATSAMD21 serieis of microcontrollers and the PCM5102 DAC. It supports SD via an SPI interface.

## Revisions and Notes
### REV 0
- DAC does not have 3.3v on VDDIO or VDDIN
- PCM_MUTE (DAC mute) is not connected to MCU or even a pull up resistor to 3.3v so DAC is always muted by default
- The hold switch was botched (not connected to MCU and wrong net for power)
- All displays sink current from the LDO instaed of the battery directly, it may be desirable to change this
- No dedicated debug port for SWCLK and SWDIO
- AMP_SHUTDOWN should be pulled low but is not
### REV 1
- should fix all major issues with REV 0
- may change placement of volume knob and power switch
