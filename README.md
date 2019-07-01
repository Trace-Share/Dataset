# Trace-Share: Dataset

Example of network traffic traces provided as annotated units.

_(This repository will be archived after Trace-Share web platform introduction.)_

### Table of Contents

* [Description](#description)
* [Traces](#traces)
   + [SSH-Hydra](#ssh-hydra)
   + [SSH-Medusa](#ssh-medusa)
   + [SSH-Ncrack](#ssh-ncrack)
* [Contribution](#contribution)


## Description

Annotated units of SSH dictionary attack performed by `medusa`, `hydra` and `ncrack` tools.


## Traces

### SSH-Hydra

Version: 8.4
Webpage: https://www.thc.org/thc-hydra/

- hydra-1_tasks.pcap
    - _command:_ `$ ./hydra -l user -x "1:5:a" -t 1 ssh://10.0.0.3/`
    - _attacker:_ 240.0.1.2
    - _defender:_ 240.125.0.2    
- hydra-4_tasks.pcap
    - _command:_ `$ ./hydra -l user -x "1:5:a" -t 4 ssh://10.0.0.3/`
    - _attacker:_ 240.0.1.3
    - _defender:_240.125.0.2 
- hydra-8_tasks.pcap
    - _command:_ `$ ./hydra -l user -x "1:5:a" -t 8 ssh://10.0.0.3/`
    - _attacker:_ 240.0.1.4
    - _defender:_ 240.125.0.2 
- hydra-16_tasks.pcap
    - _command:_ `$ ./hydra -l user -x "1:5:a" -t 16 ssh://10.0.0.3/`
    - _attacker:_ 240.0.1.5
    - _defender:_ 240.125.0.2 
- hydra-24_tasks.pcap
    - _command:_ `$ ./hydra -l user -x "1:5:a" -t 24 ssh://10.0.0.3/`
    - _attacker:_ 240.0.1.6
    - _defender:_ 240.125.0.2 
    

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

New datasets are welcome! The sharing platform is not working yet, but we can already create and share new network traffic traces.

*If you are interested in research collaborations, don't hesitate to contact us at  [https://csirt.muni.cz](https://csirt.muni.cz/about-us/contact?lang=en)!*
