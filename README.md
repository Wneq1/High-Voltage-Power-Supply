# High-Voltage-Power-Supply
High Voltage Power Supply
- BEWARE! HIGH VOLTAGE CIRCUITRY CAN BE LETHAL. DO NOT ATTEMPT TO REPLICATE WITHOUT PROPER KNOWLEDGE AND PRECAUTIONS. BY ATTEMPTING TO REPLICATE THIS CIRCUIT, YOU ASSUME ALL RISKS AND LIABILITIES ASSOCIATED WITH HIGH VOLTAGE EXPERIMENTATION.

Since I was a child, the sight of an electrical arc has always given me goosebumps and sparked immense curiosity about how to achieve such high voltage in my own workshop. Searching the internet, I found several schematics on how to build such a generator, but none of them met my expectations. So, I decided to combine a few readily available ones. My assumptions were:
• Voltage above 10kV
• Low costs (readily available parts)
• Simple circuit design if possible
• Utilization of a flyback transformer
• No direct connection to the mains
• As long-lasting operation as possible

NOTE! THE FOLLOWING PROJECT INVOLVES VERY HIGH VOLTAGES THAT ARE DANGEROUS TO THE USER'S LIFE AND HEALTH. IT IS DISCOURAGED FOR AMATEURS AND BEGINNERS WITHOUT PROPER EXPERIENCE TO ATTEMPT THIS PROJECT!!! BY CONSTRUCTING THIS CIRCUIT, YOU DO SO AT YOUR OWN RISK!

As I found an old flyback transformer in my drawer, I decided to find out what I could use it for, and quite quickly discovered that it could be used to generate high voltages. For the generator circuit, I decided to utilize the timeless NE555. I found information online about the frequency at which the flyback transformer operates, which is about 15kHz, and I decided to select the components accordingly for my generator. In the next part of the schematic, we see the circuit, or rather, the complementary driver controlling the gate of the keying MOSFET for the flyback transformer coil. As can be seen, for protection against overvoltages, a diode has been included in parallel with the primary winding, along with resistors.

Power Supply Circuit Diagram:
![image](https://github.com/Wneq1/High-Voltage-Power-Supply/assets/127328405/53c26956-a04a-405a-9484-5daf3c6c9708)

As a voltage stabilizer, I used the classic 7812. By using this stabilizer, it would be possible to power both the executive module and our generator from a single power source with the appropriate current capacity (the stabilizer would cut off disturbances related to MOSFET keying). However, I decided to isolate these two voltages.

Generator schematic:
![image](https://github.com/Wneq1/High-Voltage-Power-Supply/assets/127328405/a16f5863-6202-4186-8eb0-0acf827b7141)


Astable multivibrator circuit based on NE555, operating in the range of 10kHz to 32kHz. The frequency selection is done using a precision 10k potentiometer. There is also the possibility of modulating our high voltage through audio sound. To achieve this, connect a 100nF capacitor to pin 5 of the NE555, followed by the modulating signal, preferably from an amplifier with a power of about 0.5-1.5 W.

�
=
1.44
(
10.470
�
Ω
+
2
×
2
�
Ω
)
×
10
�
�
=
9.952
 
kHz
f= 
(10.470kΩ+2×2kΩ)×10nF
1.44
​
 =9.952kHz

�
=
1.44
(
0.470
�
Ω
+
2
×
2
�
Ω
)
×
10
�
�
=
32.215
 
kHz
f= 
(0.470kΩ+2×2kΩ)×10nF
1.44
​
 =32.215kHz

Executive module with a flyback transformer:
