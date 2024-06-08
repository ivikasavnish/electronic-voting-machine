# electronic-voting-machine

A updated EVM core which will be more secure , temper proof

Other desired performance and intigrity metrices


1. ability to perform all functionality of Indian voting machine (Election Commission of India) by default
2. ability to print intigrity hash at any time. At start , mid and end of election which contains all data including geo-tags, time, peripheral units id , person id etc
3. ability of read information from smartcard( assuming voter card ( EMV)
4. ability to retain order and time of polls and generate hash accordingly
5. confirable security mechanism
6. should be able to register each keystroke with timestamp


General usecase

1. At time of EVM configuration , evm will print some slips based on input

Inputs will be

a.  machine identity -> voting unit, control unit , loaded sequences of candidates and party symbol ( can be decrypted anytime with general predefined key)

b.  vote sequence -> can be revealed with special keys once candidate call for objection. 

c.  integrity hash -> will be printed towards end of voting and it will be shared publically to ensure trust. If any votes is manipulated, hash will be different. For every 1000 votes, there will be 1 hash will be printed. So at end of day , will have series of hashes plus  **hashes of all hash**

d. towards end of voting, a event summary will be published. which include all keystroke like polling start, controller buttons activity and voters activity. to ensure voters privacy, in final slip, for every key press on ballot unit , only a long press will be shown by vertical thick line, controller unit by big dots etc. if someone presses buttons twice,thrice or more, it will be shown also. 
e. Towards end of voting , a binary output will be generated and this could be uploaded. Some features can not be revealed like actual symbol per vote, party wise vote etc
f. Rest feature can be shown online like number of votes, timestamps, clicks , total number of register voters by matching data from evm plus already available stats
g. This will ensure tranparency and trust in voting system. no one can temper with evm because data will be changes and everyone can verify it
h.  at time of counting , there must be hash match and then if any mismatch , raise flag
i.  counting can be done online with click of button with help of special election key. Rest only VVPAT counting will be required to prove correctness. 
j. counting can be completed in 10 min. rest vvpat will be required to approve. very less pressure of election machinary and officer . very less bias
