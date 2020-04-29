# The Ploopy Safetyhub

If you're a certain kind of tinkerer, you probably have a whole bunch of computers with busted USB ports. Maybe you dropped a screwdriver on a dev board one time, or accidentally charged your EV prototype through the debugging interface. Either way, you oopsied and now your shiny Thinkpad (or Macbook, we don't judge) has a dead USB port.

A "simple" way to avoid this problem is to use a "powered" USB hub, which protects the upstream port from downstream mischief. The fact that we looked for a reliable one and couldn't find it is the reason this project exists. In short:

## The Ploopy Safetyhub was explicitly designed to protect your computer from the antics of your bus-powered devices. No more murdering the USB ports on your shiny computer!

Specifically:

- The 5V line from the upstream data port is not connected to any downstream 5V lines, so a downstream short can't damage your computer.
- The data lines have good ESD protection on both the upstream and downstream sides, serving as a first (and second) line of defense against ESD strikes.
- Downstream 5V lines have FET-based (fast, recoverable) over-current protection for downstream shorts. All downstream 5V power comes from a separate USB-C port (which would typically have a robust wall-wart plugged into it).

Spec-wise:

- 3 downstream USB 2.0 ports, including one port rated for 1.5A charging.
- Microchip USB2513B hub controller.
- Separate upstream USB-C connectors for data (USB 2.0) and power (up to 3A).
- LED indicators to indicate whether a port is active/faulted.
- No direct connections between upstream and downstream power/data lines.
- Heavy-duty ESD protection (IEC 61000-4-2 class 4).

The way it works is simple: there are no direct power/data connections between your computer and downstream devices. Power comes from a sturdy wall-wart, and beefy ESD protection makes sure nothing zappy makes it to your computer. As long as your device is bus-powered (i.e. doesn't have a power supply of its' own), the Safetyhub should protect your computer.

## Obligatory Warnings

The Safetyhub is not electrically isolated, and won't protect from high voltages, ground loops and other dangerous situations. If your downstream device has its' own power supply/has high voltages present/presents other electrical hazards, you'll need a real isolation barrier. If you're not sure if this paragraph describes your situation, please consult with someone who can help you avoid electrocution/accidents that give you superpowers.

## Under what license is this released?

The hub is released under OHL CERN v1.2. Check the respective directories for full license text.
