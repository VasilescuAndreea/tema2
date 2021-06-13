# Tema 2

- [Controlul congestiei (25%)](#congestion)
- Exercițiu la alegere (25%)
  - [Rutare](#rutare)
  - [HTTP API](#http)
- [ARP Spoofing (25%)](#arp_spoof)
- [TCP Hijacking (25%)](#tcp_hij)


<a name="congestion"></a> 
## 1. Controlul congestiei (25%)

### 1.1 Diagrama pentru RENO este:

![alt text](https://www.networkers-online.com/blog/wp-content/uploads/2016/10/STEVENS2-1024x552.jpg)

- Slow Start
- Congestion Avoidance
- Fast Retransmit 
- Fast Recovery

### 1.2 Diagrame pentru ...

- A
- B
- C


<a name="rutare"></a> 
## 2. Exercițiu la alegere (25%)

<a name="rutare"></a> 
### Rutare

- Forwarding vs. Routing 
- Link State Routing 
- Distance Vector Routing 
- Open Shortest Path First 
- Border Gateway Protocol Routing 

### 2.1 Forwarding vs Routing 
Network layer-ele fiecarui nod au 2 parti 
	1. Routing Algorithm: determina path-ul end to end prin retea ( Cum sa ajung dintr-un nod particular, in orice alt nod din retea). 
	2. Local Forwarding table

Algoritmul de routare determina path-ul end to end prin retea ( Cum sa ajung dintr-un nod particular, in orice alt nod din retea). Odata ce acest algoritm se executa la un anumit nod, acesta populeaza local forwarding table (o masa de redirectionare locala)  la nod.

Forwarding = procesul fizic de mutare al unui pachet de la o  interfata de nod, la interfata de iesire a altui nod 

Forwarding table = determina actiunea de redirectionare locala la fiecare router

In desen este un pachet care ajunge, iar inputul interfetei acestui nod este marcat cu 1 2 si 3, deoarece sunt trei interfete de iesire pentru acest nod. Orice alt pachet care ajuinge la acest nod trebuie sa plece prin 1, 2 sau 3. 

CE FACE ROUTING ALGORITHM?  Spune care pachet merge pe lungimea 3, care merge cu lungimea 2 si care merge cu lungimea 1. 

ROUTING & FORWARDING, CUM INTERACTIONEAZA ACESTEA
Odata executat algoritmul de routare, vor fi determinate urmatoarele: pentru acest interval de adrese, care este marcat in tabela ca avand intervalul de adresa 1, va trimite toate acele tabele care sunt destinate intervalului de adrese 1, impreuna cu lungimea de iesire 3. Pentru pachetele care sunt destinate pentru intervalul de adresa 2 si 3, trimite impreuna cu lungimea de iesire 2, iar pentru toate celelalte adrese, va trimite impreuna cu 1. 


### 2.2 Link State Routing

Conceputl de baza al Link State Routing ( ruta de legatura-stare) este ca fiecare nod construieste o harta a conectivitatii la retea, sub forma de grafic, care arata ce noduri sunt conectate la celelalte noduri din retea. Fiecare nod calculeaza apoi in mod independen umrmatoarea cea mai buna cale logica de la acest nod la fiecare destinatie posibila din retea. 

Pentru a avea un algoritm link state care sa functioneze, nodul trebuie sa stie reteaua completa si topologia( trebuie sa aiba imaginea completa a network-ului).  Pentru a avea cunostinte globale, trebuie transmise toate informatiile despre legatura catre toata lumea. Apoi, fieca poate independent sa ruleze acelasi algoritm, folosind aceleasi informatii de inputz, c`eea ce inseamna ca, costul fiecarei lezgaturi este preluat cu acelasi rezultat. 


<a name="http"></a> 
### HTTP API

Aplicația poate fi accesata la adresa:
```
http://ec2-34-34-34-34.compute-1.amazonaws.com/subnetting
```

<a name="arp_spoof"></a> 
## 3. ARP Spoofing (25%)

Scrieție mesajele primite de server, client și printați acțiunile pe care le face middle.
```
logs din aplicația voastră
```

Rulați pe `middle` comanda `tcpdump -SntvXX -i any` și salvați log-urile aici. Încercați să salvați doar cateva care conțin HTML-ul de la request-ul din server.
```
logs de tcpdump
```
Puteți pune și capturi de ecran din wireshark prin orice alte metode de prezentare.

<a name="tcp_hij"></a> 
## 4. TCP Hijacking (25%)
Scrieție mesajele primite de server, client și printați acțiunile pe care le face middle.
```
logs din aplicația voastră
```

Rulați pe `middle` comanda `tcpdump -SntvXX -i any` și salvați log-urile aici. Încercați să salvați doar cateva care conțin HTML-ul de la request-ul din server.
```
logs de tcpdump
```
Puteți pune și capturi de ecran din wireshark prin orice alte metode de prezentare.
