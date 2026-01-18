# Proiect_ESP
Proiectul constă în proiectarea și construcția unui robot mobil (rover) capabil să fie controlat de la distanță mare prin intermediul unui protocol radio personalizat, utilizând module ESP32 și antene externe.


# BOM (Bill Of Materials) 


| Componentă | Cantitate | Descriere / Rol în Proiect |
|---|---:|---|
| Ardunio| 2 | Unitățile centrale: una pentru telecomandă (Transmițător) și una pentru robot (Receptor). |
| Module extern NRF24L01| 2 | Arduino nu are modul Wi-fi/Bluetooth integrat. |
| Antenă Externă 2.4GHz (SMA) | 2 | Crește raza de acțiune și oferă proiectului un aspect tehnic complex. |
| Cablu Pigtail IPEX la SMA | 2 | Face legătura între conectorul mic de pe placa ESP32 și antena externă. |
| Driver de Motor L298N | 1 | Permite controlul puterii și direcției motoarelor de curent continuu. |
| Șasiu Robot (2WD sau 4WD) | 1 | Structura fizică a robotului, include motoarele și roțile. |
| Senzor Ultrasonic HC-SR04 | 1 | Folosit pentru „inteligența” robotului (evitarea automată a coliziunilor). |
| Acumulatori Li-ion 18650 (3.7V) | 2 | Sursa de alimentare principală pentru motoare și electronica robotului. |
| Modul Joystick sau Potențiometre | 1 | Interfața de control pentru utilizator (montată pe telecomandă). |
| Breadboard & Fire Jumper | 1 set | Pentru realizarea conexiunilor electrice fără lipire (în faza de prototip). |
| Regulator de tensiune (opțional) | 1 | Pentru a asigura un curent stabil de 5V către plăcile ESP32. |


# Intrebari:
Q1 - What is the system boundary?
Granița sistemului este definită de interfața dintre componentele hardware controlate și mediul extern. Aceasta include Transmitter-ul (telecomanda cu Arduino Uno, joystick și modulul radio) și Receiver-ul (șasiul robotului).
Fluxul de date intră prin User Input (joystick), este transmis prin Radio Frequency (RF) Link, și se transformă în Physical Output prin DC Motors.
Tot ce ține de reflexia semnalului ultrasonic pe obiecte sau interferențele electromagnetice externe se află în afara graniței sistemului.
<br>
Q2 - Where does intelligence live? Inteligența este distribuită, dar nucleul decizional se află în Firmware-ul încărcat pe Arduino-ul de pe robot.
Acesta execută o buclă de tip Control Loop în care procesează în timp real două surse de date: comenzile primite prin Radio Payload și datele de proximitate de la Ultrasonic Sensor.
„Inteligența” propriu-zisă constă în logica de Collision Avoidance, care poate suprascrie (override) comanda utilizatorului pentru a preveni un impact.
<br>
Q3 - What is the hardest technical problem? 
Cea mai mare provocare este gestionarea Signal Integrity și a Latency-ului în comunicația wireless. 
<br>
Q4 - What is the minimum demo?
Apasarea unui buton de pe telecomandă va rezulta intr-o miscare a masinii , rezunltand faptul ca exista comunicare intre arduino-uri
<br>
Q5-Why is this not just a tutorial?
Proiectul depășește nivelul unui tutorial deoarece implică un proces intens de Hardware Troubleshooting și Diagnosticare, forțat de utilizarea unor componente cu un grad ridicat de uzură.
