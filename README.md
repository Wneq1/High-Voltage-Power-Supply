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


Executive module with a flyback transformer:

![image](https://github.com/Wneq1/High-Voltage-Power-Supply/assets/127328405/472ee2cd-0796-414f-920f-e39cdb869145)


As we can see in our schematic, the signal after exiting the generator is fed into the complementary driver through resistor R3. The secondary driver circuit allows for greater current load capability of the MOSFET gate. Further along, we see a medium-power MOSFET IRF260 and a protection circuit to safeguard against overvoltages. It's important that the resistor connected in series with the diode is a high-power resistor due to the current flowing in the circuit. An important aspect is the number of windings wound on our flyback transformer. Online sources suggest 6-15 windings; in my project, I used 12 windings. During testing, the most optimal power supply parameters turned out to be 25V/4A. Operating under such parameters, the circuit maintained a temperature on the heatsink of less than 50 degrees Celsius for about 4 minutes.

Briefly about the enclosure:
I decided to use a plastic enclosure, in which I mounted a cable gland and built a "chamber" to separate the flyback transformer from the electronics using acrylic. I terminated the positive wire with a ring terminal and screwed it to the conductive part of the cable gland. As for the negative terminal, after prior identification, I connected it to a banana socket mounted on the rear panel of the enclosure. On the front panel, there are 4 banana sockets: two for powering the control circuit and two for powering the executive circuit. In addition to the power connectors on the front panel, there is a multi-turn potentiometer allowing us to fine-tune the operating frequency of our circuit. To improve airflow, I decided to use a small fan connected just after the 12V stabilizer. The entire board with components is soldered onto a single-sided prototyping board and secured to the enclosure using two M3 screws.

View inside the device:

![image](https://github.com/Wneq1/High-Voltage-Power-Supply/assets/127328405/96d44486-1712-4e99-8bca-53a78b7c13d4)


Device view:

![image](https://github.com/Wneq1/High-Voltage-Power-Supply/assets/127328405/0ab82661-69bd-47de-a9f3-06f17a045370)

![image](https://github.com/Wneq1/High-Voltage-Power-Supply/assets/127328405/4fc4c41b-3fd0-4eaf-8ec1-7d63981e803f)


Here are some example effects of the device's operation:
![image](https://github.com/Wneq1/High-Voltage-Power-Supply/assets/127328405/44abc55d-11ec-4253-8d65-4970f7f21ce5)

![image](https://github.com/Wneq1/High-Voltage-Power-Supply/assets/127328405/bb7f0db5-8212-4e0b-a081-1b4223a0577b)

![image](https://github.com/Wneq1/High-Voltage-Power-Supply/assets/127328405/829fe327-7aa0-4239-95c1-b4078a31a776)
