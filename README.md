# Design-of-Low-Dropout-Regulator
The LDO Regulator has been designed for a voltage of 0.9v for a load current of (0-20)mA. The design and simulation have been performed in the Cadence Virtuoso (simulator), and the technology used for the simulation is tsmcN65. 

Introduction:

The circuit diagram of the LDO architecture is as follows:

![image](https://github.com/TarakaSriram/Design-of-Low-Dropout-Regulator/assets/65438040/83839871-ff75-4900-960d-5b6db14bbb4d)


A simple LDO consists of an error amplifier (EA) and pass transistors to eliminate ripples and regulate the output voltage. LDO regulators have the smallest layout, footprint area, and low quiescent current, providing small volume and high current efficiency. Given the negative feedback control, LDO regulators can regulate the output voltage irrespective of load current and input voltage variations if the loop gain is sufficiently large.

Different types of pass transistor configurations can be possible and are used. Pass devices include NPN Darlington, NPN, PNP, N-MOSFET, P-MOSFET, and N-MOSFET with one charge pump circuit. Darlington NPN and NPN configurations are unsuitable because of their large dropout voltage. If an LDO voltage is required, then the most appropriate BJT is the PNP transistor; however, this transistor suffers from a large leakage current because of its low βp compared with the NPN transistor, which has a large βn. A MOSFET is selected to replace the BJT as the pass transistor to eliminate these two critical and obvious disadvantages. The LDO regulator requires LDO voltage and low quiescent current; the P-MOSFET is the best choice among the various configurations.The compensation complexity of an LDO regulator with N-MOSFET
is considerably lower than that of an LDO regulator with P-MOSFET.

For the operational amplifier i have designed the folded cascode configuration, pmos as the pass devies and for varying load current ipwl from Analog library has been used.

Folded cascode Opamp :  Folded cascode op amp has been used in the opamp and the single stage configuration will be used , the gain of the opamp is found to be around 40dB.
The PMOS transistors have been used as the pass transistor but in large number from tsmc N65nm technology(pch_lvt) and the resistors, capacitors are taken from the analog library.

The droop voltage depends upon the Current variation i.e more the current variation the more the droop voltage will be.
