# Transmit Diversity MIMO in Vehicular Communication
This project demonstrates how Transmit Diversity Multiple Input Multiple Output (TD MIMO) can be employed in Vehicular Communication. The simulation flow of this project is expressed with the block diagram below.

![MIMO and Convolutional Coding in DSRC](https://user-images.githubusercontent.com/3108754/150842261-93b1030f-4958-4c6e-b114-1d6ba6691e1c.JPG)

The above figure depicts the structure of the DSRC PHY layer including MIMO functionality. According to this figure data produced by the sending device is pushed to the PHY layer. The PHY layer prepares the data to be transmitted through the air medium. There are several steps in the PHY layer at the transmitter side which are FEC Coding, Signal Modulation, OFDM Modulation, and MIMO Transmitter. The FEC Coding portion converts the data bits into codeword bits using a specified coding scheme and coding rate. This project uses Convolutional Coding shceme and two coding rates are available which are 1/3 and 1/2. Then the coded data is passed through the Signal Modulation portion where the codeword bits are modulated using a specified modulation technique. This project uses QPSK modulation technique. After that, the modulated data is passed through the OFDM Modulation step where modulated data symbols are prepared to combat against interference caused by multipath fading in the air medium. OFDM Modulation and Demodulation segments are configured based on IEEE 802.11p specifications. Then, the OFDM modulated data symbols are sent through the 10 MHz channel using MIMO. This project uses two MIMO configurations which are 2x2 (two transmitting antennas and two receiving antennas) configuration and 4x4 (four transmitting antennas and four receiving antennas) configuration. MIMO Receiver block uses two equalization methods which are Zero Forcing (ZF) and Minimum Mean Squared Error (MMSE). On the receiver side, similar demodulation and decoding techniques are applied to the received data to get the best approximation of the transmitted data. The simulation results are evaluated based on two metrics which are Bit Error Rate (BER) and Throughput.

Associated files-->
* Experimental_Simulation.m -> Runs the simulation as a complete package
* System_Parameter.m -> Defines the simulation parameters
* System_Initialize.m -> Initializes the simulation objects and necessary variables
* MIMOinDSRC.m -> Contains the simulations steps shown in the above figure
* Pilot_Generator.m -> Generates pilot symbols
* Ideal_Channel_Estimation.m -> Measures channel response for equalization purpose
* ZF_Equalize.m -> Contains implementation for ZF equalization
* MMSE_Equalize.m -> Contains implementation for MMSE equalization

N.B.: If you take help from this project, please cite the following papers:
* U. K. Dey, R. Akl, and R. Chataut, “Selective MIMO in Vehicular Communication for Reliable Safety Services and High Speed Non-Safety Services,” in *2021 11th IEEE Annual Ubiquitous Computing, Electronics & Mobile Communication Conference (UEMCON),* 2021.
* U. K. Dey, R. Akl, and R. Chataut, “High Throughput Vehicular Communication Using Spatial Multiplexing MIMO,” in *2020 10th Annual Computing and Communication Workshop and Conference (CCWC), pp. 0110-0115,* 2020.
