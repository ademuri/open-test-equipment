## usb-c-banana-adapter

Adapter board for a USB-C downstream-facing port (DFP). This allow supplying
power over USB-C using a lab power supply with banana jack outputs. The USB
port uses 10k pullups on the CC pins to indicate that it can supply 5V at 3A.
Note that this does **not** follow the USB-C spec - the spec requires that a
DFP only enable power on VBUS once the DFP has confirmed a device is plugged in
by reading the voltage divider on the CC channels.


## usb-c-banana-with-data

Similar to the above, but has two USB-C ports - one upstream and one downstream
port. The data lines are connected between the ports, but power is not. Power is
injected into the DFP from banana jacks. This is useful for measuring the
conducted emissions of a USB device with a DC LISN, while sending data over USB
as well.

### USB trace impedance

Given a two-layer board and the connector geometry, it's difficult to make the USB traces have the 45Ω impedance as per the USB spec. With a trace width of 0.3mm and a (best-case) spacing of 0.2mm, and a ground plane on the other side of the 1.6mm board, the impedance is around 45Ω. The traces are within 0.5mm length of each other, with a total length of ~13mm and ~14mm for the two USB pairs. This all is probably good enough, at least for full-speed USB (12Mbps).