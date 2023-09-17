# IEEE-EDC-2023-Team-InsTech
Our team managed to secure the first place in the Electronic Design Competition 2023, organized by the IEEE Sri Lanka section.
## Final circuit
<p align="center">
  <img  src="https://github.com/avishkaherath/AMD-Module-Team-InsTech-IEEE-EDC-2023/assets/125986011/20dc8d04-2c97-43fe-9bc3-2eba483a6203">
</p>
Advanced Light Intensity Indicator (ALII) module is an innovative solution designed to monitor and indicate light intensity levels, providing an average intensity over a specific period. The goal of the final phase of the competition was to complete three given tasks in a short time period.
We were able to complete the breadboard implementation and the simulation of the full circuit with all the features in a short time period, surpassing the other teams of the competition. 
The functionality of the circuit is explained step by step using the following subcircuits.

## 8-bit ADC
<p align="center">
  <img  src="https://github.com/avishkaherath/AMD-Module-Team-InsTech-IEEE-EDC-2023/assets/125986011/0559f352-8733-4a83-9f40-4b8671943900">
</p>
The LDR circuit changes its output voltage with respect to the light intensity, and the output is fed to the 8-bit ADC circuit. In this circuit we divide the reference voltage for each comparator, and compares it with the input voltage to the circuit. After comparing the voltages, we forward them to a buffer circuit to map the comparator output between 0V to 5V.

## Charge circuit
<p align="center">
  <img  src="https://github.com/avishkaherath/AMD-Module-Team-InsTech-IEEE-EDC-2023/assets/125986011/6e6d89c1-322a-429f-a001-fa5e58134a3f">
</p>
The output of each comparator is then fed into seperate charging circuits. The caacitor in the charging circuit is charged when an input voltage is given. After charging for a period of time, if the voltage of the non-inverting input islarger than the threshold voltage given to the inverting input, the op-amp will work as a comparator and give the output.
By using this strategy we can ignore any sudden fluctuations in the light intensity on the device.

## 8 to 3 bit encoder
<p align="center">
  <img  src="https://github.com/avishkaherath/AMD-Module-Team-InsTech-IEEE-EDC-2023/assets/125986011/130394b0-cb78-4951-86aa-0718800e31d6">
</p>
The outputs from the charging circuit will then be forwarded to the 8 to 3 bit encoder. Using this encoder we can map the inputs to three bits using binary numbering system. Then these outputs are forwarded to the seven segment display driving IC.

## Seven segment input
<p align="center">
  <img  src="https://github.com/avishkaherath/AMD-Module-Team-InsTech-IEEE-EDC-2023/assets/125986011/2dd28417-fc4c-4ebc-ae0f-f4ecdbfce265">
</p>
Using the outputs given by the 8 to 3 bit encoder, this IC maps the 3 bits to 8 outputs and forwards it to the seven segment display. Then the seven segment display will display the light intensity using numbers from 0-7 where the 7 is the highest intensity level.

## Average circuit
<p align="center">
  <img  src="https://github.com/avishkaherath/AMD-Module-Team-InsTech-IEEE-EDC-2023/assets/125986011/fe230626-0621-4239-9678-72ecffa7e144">
</p>
