# usb-pmt
USB adapter for gamma scintillation detectors with photomultiplier tubes

## v1.0
### Known bugs
- With 10 MΩ PMT, the power supply can only provide around 600V. Both "on" time and duty cycle need to be higher to get the desired 1500V. This can be achieved by modifying the resistors around U3.
- Filtering capacitance for the low-voltage part of the circuit is too low. This allows noise from the USB power to propagate into the microphone input. There should be at least one 1000 µF capacitor on the power line. However, this does not seem to impact the spectrum quality.
- The green LED glares too much. Higher value of resistor should be used.
- There should be a pole-zero cancellation resistor in parallel to C13, like C10 and R23. 1 kΩ seems to work fine. It improves resolution at lower energies.
