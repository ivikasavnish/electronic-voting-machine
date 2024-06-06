# electronic-voting-machine

A updated EVM core which will be more secure , temper proof

Other desired performance and intigrity metrices


1. ability to perform all functionality of Indian voting machine (Election Commission of India) by default
2. ability to print intigrity hash at any time. At start , mid and end of election which contains all data including geo-tags, time, peripheral units id , person id etc
3. ability of read information from smartcard( assuming voter card ( EMV)
4. ability to retain order and time of polls and generate hash accordingly
5. confirable security mechanism


General usecase

1. At time of EVM configuration , evm will print some slips based on input

Inputs will be
a. machine identity -> voting unit, control unit , loaded sequences of candidates and party symbol ( can be decrypted anytime with general predefined key)
b. vote sequence -> can be revealed with special keys once candidate call for objection. 
c. integrity hash -> will be printed towards end of voting and it will be shared publically to ensure trust. If any votes is manipulated, hash will be different. For every 1000 votes, there will be 1 hash will be printed. So at end of day , will have series of hashes plus  hashes of all hash.

d. at time of counting , there must be hash match and then if any mismatch , raise flag
