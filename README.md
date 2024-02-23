# High-Voltage-Power-Supply
High Voltage Power Supply

Since I was a child, the sight of an electrical arc has always given me goosebumps and sparked immense curiosity about how to achieve such high voltage in my own workshop. Searching the internet, I found several schematics on how to build such a generator, but none of them met my expectations. So, I decided to combine a few readily available ones. My assumptions were:
• Voltage above 10kV
• Low costs (readily available parts)
• Simple circuit design if possible
• Utilization of a flyback transformer
• No direct connection to the mains
• As long-lasting operation as possible
- BEWARE! High voltage circuitry can be lethal. Do not attempt to replicate without proper knowledge and precautions. By attempting to replicate this circuit, you assume all risks and liabilities associated with high voltage experimentation.

NOTE! The following project involves very high voltages that are dangerous to the user's life and health. It is discouraged for amateurs and beginners without proper experience to attempt this project!!! By constructing this circuit, you do so at your own risk!

As I found an old flyback transformer in my drawer, I decided to find out what I could use it for, and quite quickly discovered that it could be used to generate high voltages. For the generator circuit, I decided to utilize the timeless NE555. I found information online about the frequency at which the flyback transformer operates, which is about 15kHz, and I decided to select the components accordingly for my generator. In the next part of the schematic, we see the circuit, or rather, the complementary driver controlling the gate of the keying MOSFET for the flyback transformer coil. As can be seen, for protection against overvoltages, a diode has been included in parallel with the primary winding, along with resistors.

Power Supply Circuit Diagram:
