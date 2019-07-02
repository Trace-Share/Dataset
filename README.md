# Trace-Share: Dataset

Example of network traffic traces provided as annotated units.

_(This repository will be archived after the launch of the sharing platform.)_

### Table of Contents

* [Description](#description)
* [Traces](#traces)
   + [SSH-Hydra](#ssh-hydra)
   + [SSH-Medusa](#ssh-medusa)
   + [SSH-Ncrack](#ssh-ncrack)
* [Contribution](#contribution)


## Description

This repository contains an example of so-called _annotated units_ composed of network traffic trace with interest-related packets only. While the real-world traffic capture needs to be kept private, the _annotated units_ can be freely shared since they only contain the interest-based trace of traffic with a minimum of private information.

All _annotated units_ are normalized network traffic traces where MAC and IP addresses are changed uniformly to the same address range between all units. Moreover, the timestamp of the capture is set to zero epoch time to ease further injection of the unit to the real-world background traffic.

This repository provides an example of selected _annotated units_ generated by [Trace-Creator](https://github.com/Trace-Share/Trace-Creator) or extracted from real-world network traffic. The aim is to facilitate understanding of the new concept of _annotated units_ and _semi-labeled datasets_.


## Traces

The following examples contain SSH dictionary attack performed by commonly available tools and generated using [Trace-Creator](https://github.com/Trace-Share/Trace-Creator). IP addresses are adjusted to ease recognition of different attack types for use-case when traces are merged using the simple [mergecap](https://www.wireshark.org/docs/man-pages/mergecap.html) tool. Use our tool [Trace-Share: ID2T](https://github.com/Trace-Share/ID2T) if you want to insert these units so that they are indistinguishable in background traffic.

### SSH-Hydra

**Common description:**

Webpage: [https://github.com/vanhauser-thc/thc-hydra](https://github.com/vanhauser-thc/thc-hydra)
Software version: 8.4

**Examples:**

#### [hydra-1_tasks.pcap](./SSH-Hydra/hydra-1_tasks.pcap)

* Command: `$ ./hydra -l user -x "1:5:a" -t 1 ssh://10.0.0.3/`
* Source address: 240.0.1.2
* Destination address: 240.125.0.2

#### [hydra-4_tasks.pcap](./SSH-Hydra/hydra-4_tasks.pcap)

* Command: `$ ./hydra -l user -x "1:5:a" -t 4 ssh://10.0.0.3/`
* Source address: 240.0.1.3
* Destination address: 240.125.0.2 

#### [hydra-8_tasks.pcap](./SSH-Hydra/hydra-8_tasks.pcap)

* Command: `$ ./hydra -l user -x "1:5:a" -t 8 ssh://10.0.0.3/`
* Source address: 240.0.1.4
* Destination address: 240.125.0.2 

#### [hydra-16_tasks.pcap](./SSH-Hydra/hydra-16_tasks.pcap)

* Command: `$ ./hydra -l user -x "1:5:a" -t 16 ssh://10.0.0.3/`
* Source address: 240.0.1.5
* Destination address: 240.125.0.2 

#### [hydra-24_tasks.pcap](./SSH-Hydra/hydra-24_tasks.pcap)

* Command: `$ ./hydra -l user -x "1:5:a" -t 24 ssh://10.0.0.3/`
* Source address: 240.0.1.6
* Destination address: 240.125.0.2 
    

### SSH-Medusa 

Version: 2.2
Webpage: http://foofus.net/goons/jmk/medusa/medusa.html  

- medusa-1_tasks.pcap
    - _command:_ `$ medusa -M ssh -u user -P <passwords.txt> -h 10.0.0.3 -t 1`
    - _attacker:_ 240.0.2.2
    - _defender:_ 240.125.0.2 
- medusa-4_tasks.pcap
    - _command:_ `$ medusa -M ssh -u user -P <passwords.txt> -h 10.0.0.3 -t 4`
    - _attacker:_ 240.0.2.3
    - _defender:_ 240.125.0.2 
- medusa-8_tasks.pcap
    - _command:_ `$ medusa -M ssh -u user -P <passwords.txt> -h 10.0.0.3 -t 8`
    - _attacker:_ 240.0.2.4
    - _defender:_ 240.125.0.2 
- medusa-16_tasks.pcap
    - _command:_ `$ medusa -M ssh -u user -P <passwords.txt> -h 10.0.0.3 -t 16`
    - _attacker:_ 240.0.2.5
    - _defender:_ 240.125.0.2 
- medusa-24_tasks.pcap
    - _command:_ `$ medusa -M ssh -u user -P <passwords.txt> -h 10.0.0.3 -t 24`
    - _attacker:_ 240.0.2.6
    - _defender:_ 240.125.0.2         

            
### SSH-Ncrack

Version: 0.5
Webpage: https://nmap.org/ncrack/ 
            
- ncrack-paranoid.pcap
    - _command:_ `$ ncrack --user user1,user2,user3 10.0.0.3:22 -T paranoid`
    - _attacker:_ 240.0.3.2
    - _defender:_ 240.125.0.2 
- ncrack-sneaky.pcap
    - _command:_ `$ ncrack --user user1,user2,user3 10.0.0.3:22 -T sneaky`
    - _attacker:_ 240.0.3.3
    - _defender:_ 240.125.0.2 
- ncrack-polite.pcap
    - _command:_ `$ ncrack --user user1,user2,user3 10.0.0.3:22 -T polite`
    - _attacker:_ 240.0.3.4
    - _defender:_ 240.125.0.2 
- ncrack-normal.pcap
    - _command:_ `$ ncrack --user user1,user2,user3 10.0.0.3:22 -T normal`
    - _attacker:_ 240.0.3.5
    - _defender:_ 240.125.0.2 
- ncrack-aggressive.pcap
    - _command:_ `$ ncrack --user user1,user2,user3 10.0.0.3:22 -T aggressive`
    - _attacker:_ 240.0.3.6
    - _defender:_ 240.125.0.2   


## Contribution

New datasets are welcome! The sharing platform is not working yet, but we can prepare network traffic traces now.

*If you are interested in research collaborations, don't hesitate to contact us at  [https://csirt.muni.cz](https://csirt.muni.cz/about-us/contact?lang=en)!*
