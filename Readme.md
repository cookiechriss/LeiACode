# LeiA ProVerif and StatVerif Code Samples

This project contains the ProVerif and StatVerif code samples that I used during my Protocol Verification Research Internship for IoT Devices within cars. The code was for proving a new protocol named LeiA: A Lightweight Authentication Protocol for CAN.

### What is ProVerif
[ProVerif](http://prosecco.gforge.inria.fr/personal/bblanche/proverif/) is a software tool for automated reasoning about the security properties found in cryptographic protocols. This is a tool written in OCaml that has a bunch of cool features such as queries and events. This code was tested in version 1.94pl1
### What is StatVerif
StatVerif is an extension of ProVerif that is currently been developed at the University of Birmingham by [Eike Ritter](https://www.cs.bham.ac.uk/~exr/), my supervisor. This extension adds a few features but mainly the ability to model states. 
### What is LeiA
This  is  where  LeiA  comes  in.   LeiA  is  a  lightweight  authentication  protocol  that  has  been  proposed  in  [a paper](http://inaradu.com/publications/LeiA_A_Lightweight_Authentication_Protocol_for_CAN.pdf) by [Flavio D. Garcia](https://www.cs.bham.ac.uk/~garciaf/) and [Andreea-Ina Radu](http://inaradu.com/) at the University of Birmingham.  It works by using MAC codes to authenticate the source of the messages.  Although there have been other protocols or ways to secure the CAN bus, this is one of theonly one which is fully backwards compatible to the previous can standard and also doesn't require any additional hardware/complexity or expensive changes to be made to a vehicle.
### Results
ProVerif couldn't accurately represent the LeiA Protocol as it was not possible to model states. After creating the ProVerif code, I recreated it using StatVerif so this could work with states. There are a couple of issues with the current version however as this was built using an older version of ProVerif and as such couldn't fully verify the LeiA Protocol using the current version of StatVerif. 

