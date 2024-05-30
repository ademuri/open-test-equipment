## usb-c-banana-adapter

Adapter board for a USB-C downstream-facing port (DFP). This allow supplying
power over USB-C using a lab power supply with banana jack outputs. The USB
port uses 10k pullups on the CC pins to indicate that it can supply 5V at 3A.
Note that this does **not** follow the USB-C spec - the spec requires that a
DFP only enable power on VBUS once the DFP has confirmed a device is plugged in
by reading the voltage divider on the CC channels.

